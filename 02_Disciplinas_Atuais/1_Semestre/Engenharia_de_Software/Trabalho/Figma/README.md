# Figma — Protótipo do Poupi

- **Arquivo (edição):** https://www.figma.com/design/DnGzwIqbQO0d4Wb0ymdqYV/Poupi
- **Protótipo da Sprint 3:** https://www.figma.com/proto/DnGzwIqbQO0d4Wb0ymdqYV/Poupi?node-id=186-52&starting-point-node-id=186%3A52
- **Protótipo da Sprint 2:** https://www.figma.com/proto/DnGzwIqbQO0d4Wb0ymdqYV/Poupi?node-id=174-45&starting-point-node-id=174%3A45
- **Protótipo da Sprint 1:** https://www.figma.com/proto/DnGzwIqbQO0d4Wb0ymdqYV/Poupi?node-id=1-32&starting-point-node-id=1%3A32

Cada sprint tem uma página própria no arquivo: **"Sprint 1 - Protótipo"**, **"Sprint 2 - Protótipo"** e **"Sprint 3 - Protótipo"**. A página de uma sprint entregue não é mais alterada.

---

## Sprint 3

Catálogo com as 12 cores da Sprint 2 e 39 telas, lado a lado, 8 por linha. A barra de abas passou a ter 4 abas (Início · Lançamentos · Relatórios · Grupos), com o + flutuante; Início, Lançamentos e Relatórios rolam com as abas fixas. Os dados de exemplo são da usuária Eloisa, sem e-mail. Nas telas que rolam, o print mostra a tela inteira.

| Paleta | Carregamento | Login | Biometria |
|---|---|---|---|
| ![](Telas/Sprint_3/00-paleta-de-cores.png) | ![](Telas/Sprint_3/01-carregamento.png) | ![](Telas/Sprint_3/02-login.png) | ![](Telas/Sprint_3/03-biometria.png) |

| Criar conta | Esqueci senha | Início | Início (saldo oculto) |
|---|---|---|---|
| ![](Telas/Sprint_3/04-criar-conta.png) | ![](Telas/Sprint_3/05-esqueci-senha.png) | ![](Telas/Sprint_3/06-inicio.png) | ![](Telas/Sprint_3/07-inicio-saldo-oculto.png) |

| Selecionar mês | Notificações | Lançamentos | Lançamentos (receitas) |
|---|---|---|---|
| ![](Telas/Sprint_3/08-selecionar-mes.png) | ![](Telas/Sprint_3/09-notificacoes.png) | ![](Telas/Sprint_3/10-lancamentos.png) | ![](Telas/Sprint_3/11-lancamentos-receitas.png) |

| Lançamentos (despesas) | Busca de lançamentos | Detalhe do lançamento | Editar lançamento |
|---|---|---|---|
| ![](Telas/Sprint_3/12-lancamentos-despesas.png) | ![](Telas/Sprint_3/13-busca-de-lancamentos.png) | ![](Telas/Sprint_3/14-detalhe-do-lancamento.png) | ![](Telas/Sprint_3/15-editar-lancamento.png) |

| Confirmar exclusão | Lançamento salvo | Lançamento excluído | Despesas fixas |
|---|---|---|---|
| ![](Telas/Sprint_3/16-confirmar-exclusao.png) | ![](Telas/Sprint_3/17-lancamentos-lancamento-salvo.png) | ![](Telas/Sprint_3/18-lancamentos-lancamento-excluido.png) | ![](Telas/Sprint_3/19-despesas-fixas.png) |

| Detalhe da conta | Novo lançamento | Nova receita | Selecionar grupo (receitas) |
|---|---|---|---|
| ![](Telas/Sprint_3/20-detalhe-da-conta.png) | ![](Telas/Sprint_3/21-novo-lancamento.png) | ![](Telas/Sprint_3/22-nova-receita.png) | ![](Telas/Sprint_3/23-selecionar-grupo-receitas.png) |

| Nova despesa | Selecionar grupo | Grupos | Grupos (receitas) |
|---|---|---|---|
| ![](Telas/Sprint_3/24-nova-despesa.png) | ![](Telas/Sprint_3/25-selecionar-grupo.png) | ![](Telas/Sprint_3/26-grupos.png) | ![](Telas/Sprint_3/27-grupos-receitas.png) |

| Detalhe do grupo | Limite do grupo | Novo grupo | Relatórios |
|---|---|---|---|
| ![](Telas/Sprint_3/28-detalhe-do-grupo.png) | ![](Telas/Sprint_3/29-limite-do-grupo.png) | ![](Telas/Sprint_3/30-novo-grupo.png) | ![](Telas/Sprint_3/31-relatorios.png) |

| Selecionar período | Menu de opções | Trocar de conta | Meu perfil |
|---|---|---|---|
| ![](Telas/Sprint_3/32-selecionar-periodo.png) | ![](Telas/Sprint_3/33-menu-de-opcoes.png) | ![](Telas/Sprint_3/34-trocar-de-conta.png) | ![](Telas/Sprint_3/35-meu-perfil.png) |

| Trocar foto | Alterar senha | Formas de pagamento | Configurações |
|---|---|---|---|
| ![](Telas/Sprint_3/36-trocar-foto.png) | ![](Telas/Sprint_3/37-alterar-senha.png) | ![](Telas/Sprint_3/38-formas-de-pagamento.png) | ![](Telas/Sprint_3/39-configuracoes.png) |

### Fluxo do protótipo (começa em Carregamento, 151 interações)

| De | Ação | Para |
|---|---|---|
| Carregamento | depois de 1,5 s | Login |
| Login · Entrar / Biometria · sensor / Criar conta | clique | Início |
| Abas · + · foto do perfil | clique | a aba escolhida · Novo lançamento · Menu de opções (Meu perfil, Trocar de conta, Sair) |
| Início · olho / mês / sino | clique | saldo oculto · Selecionar mês · Notificações (cada aviso abre a tela certa) |
| Início · próximas contas / Ver todas | clique | Detalhe da conta (Marcar como paga) · Despesas fixas |
| Lançamentos · filtros / lupa | clique | extrato de receitas ou de despesas, Despesas fixas · Busca |
| Lançamento (extrato, busca, histórico, detalhe do grupo) | clique | Detalhe do lançamento → Editar ou Excluir (com confirmação) |
| Salvar / Excluir | clique | mensagem "Lançamento salvo" ou "Lançamento excluído", que volta ao extrato em 2 s |
| Relatórios · período | clique | Selecionar período (Este mês, 3 ou 6 meses, ano, datas) |
| Meu perfil | clique | Trocar foto, Alterar senha, Formas de pagamento, Configurações, Sair |
| Grupos · filtro / grupo / Novo grupo | clique | Grupos (receitas) · Detalhe do grupo → Limite do grupo · Novo grupo |
| Setas de voltar | clique | tela anterior |

As 10 janelas que abrem por cima usam fundo escurecido e fecham ao clicar fora. "Exportar PDF", "+ Adicionar forma de pagamento" e as chaves liga/desliga mostram o lugar e o estado da função, sem tela própria.

---

## Sprint 2

Catálogo com 12 cores (entraram o gelo `#F3F7F5` e o amarelo `#E0A526`) e 19 telas, com os ajustes pedidos na apresentação: barra do limite de uma cor só com a marca "|", abas Início · Lançamentos · Grupos com o + flutuante, foto do perfil com trocar de conta, grupos de receita com filtro e menos botões repetidos.

| Paleta | Carregamento | Login | Biometria |
|---|---|---|---|
| ![](Telas/Sprint_2/00-paleta-de-cores.png) | ![](Telas/Sprint_2/01-carregamento.png) | ![](Telas/Sprint_2/02-login.png) | ![](Telas/Sprint_2/03-biometria.png) |

| Criar conta | Esqueci senha | Grupos | Grupos (receitas) |
|---|---|---|---|
| ![](Telas/Sprint_2/04-criar-conta.png) | ![](Telas/Sprint_2/05-esqueci-senha.png) | ![](Telas/Sprint_2/06-grupos.png) | ![](Telas/Sprint_2/07-grupos-receitas.png) |

| Menu de opções | Trocar de conta | Detalhe do grupo | Limite do grupo |
|---|---|---|---|
| ![](Telas/Sprint_2/08-menu-de-opcoes.png) | ![](Telas/Sprint_2/09-trocar-de-conta.png) | ![](Telas/Sprint_2/10-detalhe-do-grupo.png) | ![](Telas/Sprint_2/11-limite-do-grupo.png) |

| Novo grupo | Lançamentos | Novo lançamento | Nova receita |
|---|---|---|---|
| ![](Telas/Sprint_2/12-novo-grupo.png) | ![](Telas/Sprint_2/13-lancamentos.png) | ![](Telas/Sprint_2/14-novo-lancamento.png) | ![](Telas/Sprint_2/15-nova-receita.png) |

| Selecionar grupo (receitas) | Nova despesa | Selecionar grupo | Nova despesa (acima do limite) |
|---|---|---|---|
| ![](Telas/Sprint_2/16-selecionar-grupo-receitas.png) | ![](Telas/Sprint_2/17-nova-despesa.png) | ![](Telas/Sprint_2/18-selecionar-grupo.png) | ![](Telas/Sprint_2/19-nova-despesa-acima-do-limite.png) |

### Fluxo do protótipo (começa em Carregamento, 52 interações)

| De | Ação | Para |
|---|---|---|
| Carregamento | depois de 1,5 s | Login |
| Login · Entrar | clique | Grupos |
| Login · Entrar com biometria | clique | abre Biometria por cima; o sensor leva a Grupos |
| Login · Cadastre-se / Esqueci minha senha | clique | Criar conta / Esqueci senha |
| Grupos · filtro Receitas / Despesas | clique | Grupos (receitas) ⇄ Grupos |
| Grupos · qualquer grupo | clique | Detalhe do grupo → Editar limite → Limite do grupo → Salvar |
| Grupos · Novo grupo | clique | Novo grupo → Criar grupo → Grupos |
| Foto do perfil | clique | Menu de opções: Trocar de conta, Sair da conta |
| Barra de abas · + | clique | Lançamentos ⇄ Grupos · Novo lançamento (Nova receita / Nova despesa) |
| Nova despesa · campo Grupo | clique | abre Selecionar grupo; Entretenimento leva à despesa acima do limite |
| Salvar receita / Salvar despesa | clique | Lançamentos |
| Setas de voltar | clique | tela anterior |

As janelas que abrem por cima usam fundo escurecido e fecham ao clicar fora.

---

## Sprint 1

Catálogo de cores (10 cores e a fonte Inter) e 6 telas: Carregamento, Login, Grupos, Nova receita, Nova despesa (360 × 800) e Selecionar grupo (janela por cima da Nova despesa).

| Paleta | Carregamento | Login | Grupos |
|---|---|---|---|
| ![](Telas/Sprint_1/00-paleta-de-cores.png) | ![](Telas/Sprint_1/01-carregamento.png) | ![](Telas/Sprint_1/02-login.png) | ![](Telas/Sprint_1/03-grupos.png) |

| Nova receita | Nova despesa | Selecionar grupo |
|---|---|---|
| ![](Telas/Sprint_1/04-nova-receita.png) | ![](Telas/Sprint_1/05-nova-despesa.png) | ![](Telas/Sprint_1/06-selecionar-grupo.png) |

### Fluxo do protótipo (começa em Carregamento)

| De | Ação | Para |
|---|---|---|
| Carregamento | depois de 1,5 s | Login |
| Login · Entrar | clique | Grupos |
| Grupos · + Receita | clique | Nova receita |
| Grupos · + Despesa | clique | Nova despesa |
| Nova despesa · campo Grupo | clique | abre Selecionar grupo por cima (fundo escurecido, fecha ao clicar fora) |
| Selecionar grupo · um grupo ou X | clique | fecha o seletor |
| Salvar receita / Salvar despesa | clique | Grupos |
| Setas de voltar | clique | tela anterior |

"+ Novo grupo" e "Criar novo grupo" aparecem nas telas, mas só ganharam ligação na Sprint 2.
