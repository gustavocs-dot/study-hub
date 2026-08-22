# Site de Estudos Pessoal

Aplicação web que mantenho como projeto pessoal, hospedada na Cloudflare e usada
no dia a dia do curso. Ela reúne o material das disciplinas em três formas de
estudo: resumo, flashcard e mapa mental.

O site é um arquivo HTML único, sem framework, sem build e sem dependência
externa. O conteúdo fica num banco na nuvem, e o mesmo arquivo aberto por duplo
clique continua funcionando offline, em modo leitura.

## O que tem dentro

| Item | Quantidade |
|---|---|
| Disciplinas | 5 |
| Matérias | 8 |
| Tópicos de resumo | 76 |
| Flashcards | 377 |
| Mapas mentais | 8, com 304 caixas |
| Front-end | 3.127 linhas, num arquivo só |
| Back-end | 5 arquivos |

Todo esse conteúdo saiu dos slides e apostilas das disciplinas, resumido e
transformado em flashcard e mapa.

## Como foi construído

Front-end: HTML, CSS e JavaScript puro, sem framework e sem etapa de build.
Hospedagem: Cloudflare Pages, no plano gratuito.
Banco: Cloudflare D1.
Servidor: Cloudflare Functions, com quatro endpoints e um módulo de autenticação.
Autenticação: senha em PBKDF2-SHA256, sessão em token HMAC assinado, cookie HttpOnly.

## Decisões de arquitetura

**Ponto único de acesso a dados.** Todo acesso a armazenamento passa por um só
objeto do código. Quando troquei o armazenamento do navegador por servidor, as
treze chamadas de gravação espalhadas pelo arquivo não mudaram uma linha. A
migração saiu barata porque essa fronteira já existia antes de eu precisar dela.

**A edição é barrada no servidor, não na interface.** Esconder botões é conforto
visual. Quem recusa a gravação é o endpoint, que exige cookie válido. Testei
forçando a permissão para verdadeira dentro do navegador: a interface de edição
inteira apareceu, e a gravação voltou 401.

**Conflito de escrita detectado por número de revisão.** Cada gravação envia a
revisão em que se baseou, e o banco só aceita se ainda for aquela. Se duas telas
gravam ao mesmo tempo, a segunda recebe aviso e a opção de baixar o que fez, ao
invés de sobrescrever a primeira em silêncio.

**Um formato de dados, três visualizações.** Resumo, flashcard e mapa mental saem
da mesma modelagem. Os quatro tipos de bloco, que são parágrafo, subtítulo,
citação e lista, passam pela mesma função de renderização no resumo e na ponta do
mapa. Mexer num tipo de bloco muda os dois lugares de uma vez, que é o ponto.

**A sessão vence pelo servidor, não pelo navegador.** O cookie some quando o
navegador fecha, e o prazo de 12 horas está assinado dentro do próprio token.
São duas proteções somadas, pois a primeira depende do navegador se comportar, e
alguns preservam a sessão ao reabrir.

**Offline é modo leitura, de propósito.** Aberto por duplo clique, o arquivo
mostra a última cópia que passou por aquele navegador e não deixa editar. Ele não
tem como saber se o servidor andou desde então, e gravar por cima às cegas seria
pior que não gravar.

**A geometria do mapa impede o erro, ao invés de corrigir.** A primeira versão
ligava o centro de uma caixa ao centro da outra, e o traço atravessava o texto. A
correção não foi recortar a linha. Passei a regra a ser outra: todo traço sai da
borda direita de uma caixa e entra pela borda esquerda da seguinte, numa curva de
alças horizontais. Uma curva assim fica contida entre os dois pontos, então
atravessar uma caixa deixou de ser possível por construção.

**Testes que rodam sem navegador.** Dois scripts em Node extraem as funções
direto do HTML e conferem a geometria das curvas e a sintaxe dos scripts. Rodam
no protótipo e no arquivo publicado, com o mesmo comando.

## Limites conhecidos

O documento inteiro é gravado numa linha só do banco. Funciona bem no tamanho
atual, mas não escalaria para muitos usuários, pois cada gravação reescreve tudo.
Foi decisão consciente: o site tem um dono que edita, e o resto só lê.

Os slides e apostilas originais não vão para o repositório nem para o site, pois
são material de aula de terceiros. O que é publicado é o resumo, o flashcard e o
mapa que eu produzi a partir deles.
