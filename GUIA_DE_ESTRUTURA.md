# Guia de Estrutura

Como este repositório é organizado e por quê. Escrito para que qualquer pessoa
saiba onde encontrar um arquivo, e para que eu saiba onde guardar o próximo.

## As quatro regras

1. **`01_Apresentacao_e_Perfil` guarda os documentos de apresentação** —
   currículo, card de contato e portfólio. É o que fala de mim, e não de uma
   disciplina ou de um projeto.
2. **Toda disciplina tem `Materiais_Didaticos`** — slides, apostilas e PDFs
   disponibilizados pelo professor. É material *recebido*.
3. **Disciplina teórica acrescenta o par** `Atividades_e_Entregas`, com o que
   foi *entregue* e avaliado, e `Anotacoes_e_Resumos`, com o que eu *produzi*
   estudando.
4. **Disciplina de projeto acrescenta as etapas.** O Bootcamp I tem três
   entregas encadeadas, e organizar por etapa reflete como o trabalho acontece.

A separação entre material **recebido**, **produzido** e **entregue** é o que
sustenta a estrutura: cada arquivo tem um lugar previsível, e o lugar diz o que
o arquivo é.

## Por que existe o nível de semestre

O curso tem oito semestres. Sem esse nível, a pasta `02_Disciplinas_Atuais`
viraria um depósito já no semestre seguinte.

## Convenções de nomenclatura

- Pastas em `Snake_Case_Com_Iniciais_Maiusculas`
- Prefixo numérico (`01_`, `02_`) onde a ordem importa, para que a ordem
  alfabética coincida com a ordem lógica
- Sem acentos, espaços ou caracteres especiais — evita quebra em URL, em Git e
  em sistemas sensíveis a maiúsculas
- Arquivos em `minusculo-com-hifen.md`
- Datas sempre no formato `AAAA-MM-DD`, que ordena sozinho
- Um `README.md` por pasta, explicando o que vive ali

## A árvore

```
study-hub/
├── 01_Apresentacao_e_Perfil/
├── 02_Disciplinas_Atuais/
│   └── 1_Semestre/
│       ├── Bootcamp_I/
│       │   ├── 01_Entrega_Inicial/
│       │   ├── 02_Entrega_Intermediaria/
│       │   ├── 03_Entrega_Final/
│       │   └── Materiais_Didaticos/
│       ├── Banco_de_Dados_I/
│       │   ├── Atividades_e_Entregas/
│       │   ├── Anotacoes_e_Resumos/
│       │   └── Materiais_Didaticos/
│       ├── Engenharia_de_Software/
│       ├── Fundamentos_da_Engenharia/
│       ├── Introducao_a_Computacao/
│       └── Logica_de_Programacao/
└── 03_Projetos_e_Certificados/
    ├── Projetos/
    │   └── Site_de_Estudos_Pessoal/
    └── Certificados/
```

As cinco disciplinas teóricas seguem o mesmo padrão de `Banco_de_Dados_I`.
