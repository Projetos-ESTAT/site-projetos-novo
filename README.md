# Site de Projetos da ESTAT

Site da Diretoria de Projetos da ESTAT, feito em [Quarto](https://quarto.org).

## Como rodar localmente

1. Instale o Quarto (1.6 ou mais recente).
2. Na pasta do projeto, rode `quarto preview` para abrir o site no navegador com atualização automática.
3. Para gerar a versão final, rode `quarto render`. O resultado vai para `_site/`, que não é versionado.

## Estrutura

| Pasta / arquivo | O que tem |
|---|---|
| `_quarto.yml` | Configuração do site e menu |
| `_variables.yml` | **Todos os links usados no site** (planilhas, Pipefy, formulários...) |
| `assets/estat.scss` | Tema visual (cores e fontes da ESTAT) |
| `assets/img/` | Logo e imagens compartilhadas |
| `index.qmd` | Página inicial |
| `jornadas/` | Jornada do gerente, jornada do alocado e checklist |
| `guias/` | Comunicação com o cliente |
| `diretoria/` | História da Diretoria |

## Como adicionar uma página

1. Crie o `.qmd` na pasta da seção certa, com `title` e `description` no cabeçalho.
2. Adicione a página ao menu em `_quarto.yml`.
3. Imagens da página ficam numa pasta `images/` ao lado dela, com nomes descritivos (`alocacao-slack.png`, não `Captura de Tela...png`) e de preferência com menos de 500 KB.

## Como atualizar um link

Os links do site ficam todos em `_variables.yml`. Quando uma planilha, um formulário ou uma pasta mudar, troque o endereço lá. Todas as páginas que usam aquele link se atualizam sozinhas.

Para usar um link numa página: `[texto do link]({{< var links.nome-do-link >}})`.

## Publicação

O site é publicado automaticamente no GitHub Pages a cada push na branch `main`, pelo fluxo em `.github/workflows/publicar.yml`. Não é preciso rodar nada no computador: depois do push, o site atualiza sozinho em poucos minutos. Para acompanhar, veja a aba **Actions** do repositório.
