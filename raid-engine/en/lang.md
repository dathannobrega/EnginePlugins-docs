# Language Files

RaidEngine loads all language files from `plugins/RaidEngine/lang/`.

- File name: `<locale>.yml` (example: `en_US.yml`, `pt_BR.yml`).
- Default locale: set in `config.yml` at `raidengine.locale` (example: `en_US`).
- Fallback: if the configured locale is missing, `en_US.yml` is used.
- First run: the plugin seeds `en_US.yml` and `pt_BR.yml` automatically.

To add a language:
1. Copy an existing file in `plugins/RaidEngine/lang/`.
2. Translate the values, keeping keys/placeholders.
3. Set `raidengine.locale` to the new code and reload.

Tip: keep two‑space indentation and use MiniMessage tags for colors (e.g., `<yellow>`, `<red>`).

