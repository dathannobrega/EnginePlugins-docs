# Idiomas (Lang)

O RaidEngine carrega todos os arquivos de idioma a partir de `plugins/RaidEngine/lang/`.

- Nome do arquivo: `<locale>.yml` (ex.: `pt_BR.yml`, `en_US.yml`).
- Idioma padrão: configurado em `config.yml` na chave `raidengine.locale` (ex.: `pt_BR`).
- Fallback: se o arquivo do idioma configurado não existir, usa‐se `en_US.yml`.
- Primeira execução: o plugin cria automaticamente `en_US.yml` e `pt_BR.yml`.

Para adicionar um idioma:
1. Copie um arquivo existente em `plugins/RaidEngine/lang/`.
2. Traduza os valores, mantendo chaves/placeholders.
3. Defina `raidengine.locale` para o novo código e recarregue.

Dica: mantenha indentação de dois espaços e use tags MiniMessage para cores (ex.: `<yellow>`, `<red>`).

