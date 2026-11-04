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
| `assets/estat.scss` | Tema visual (cores e fontes da ESTAT) |
| `assets/img/` | Logo e imagens compartilhadas |
| `index.qmd` | Página inicial |
| `jornadas/` | Jornadas do gerente por produto e do alocado |
| `guias/` | Guias de comunicação e de ferramentas |
| `ferramentas/` | Checklist do gerente |
| `casos/` | Papos sobre projetos |
| `diretoria/` | História e equipe |

## Como adicionar uma página

1. Crie o `.qmd` na pasta da seção certa, com `title` e `description` no cabeçalho.
2. Adicione a página ao menu em `_quarto.yml`.
3. Imagens da página ficam numa pasta `images/` ao lado dela, com nomes descritivos (`alocacao-slack.png`, não `Captura de Tela...png`) e de preferência com menos de 500 KB.
