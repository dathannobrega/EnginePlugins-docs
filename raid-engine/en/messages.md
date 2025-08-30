# Messages

All texts are loaded from `plugins/RaidEngine/lang/*.yml`. By default the plugin seeds `en_US.yml` and `pt_BR.yml` on first run. You can add new locales by dropping more `.yml` files in that folder.

## Structure

Each file is named `<locale>.yml`, where `<locale>` is a code like `en_US` or `pt_BR`. The keys are organized in nested sections:

```yml
clan:
  command:
    create:
      success: '<green>Clan created.'
```
Always use an indent of **two spaces**. The texts can contain:
- **Colors**: use [MiniMessage](https://docs.adventure.kyori.net/minimessage/format.html) tags like `<red>` and `<green>`.
- **Placeholders**: keep markers like `%amount%`, `%player%`, or `{clan}` intact; they are replaced automatically.

Strings with colons, special symbols, or colors should be enclosed in single quotes (`'text'`).

## Default language (`raidengine.locale`)

In the `config.yml` file, choose the language to be loaded by default:

```yml
raidengine:
  locale: en_US
```

After saving, restart the server or use `/raidadmin reload`.

## Adding new languages

1. Copy an existing file in the `lang` folder, for example:
   ```bash
   cp plugins/RaidEngine/lang/en_US.yml plugins/RaidEngine/lang/es_ES.yml
   ```
2. Translate each entry, preserving keys, colors, and placeholders.
3. Set `raidengine.locale` to the new code (`es_ES`).
4. Restart the server or `/raidadmin reload`.

## Editing example

To change the clan bank deposit message:

```yml
clan:
  bank:
    deposit_success: '<green>Deposit successful!'
```

## Cautions and formatting

- Do not use tabs; only spaces.
- Colors and formatting must follow the MiniMessage standard.
- Always check placeholders and keys before saving.

## Backup tips

Before modifying any file:

```bash
cp plugins/RaidEngine/lang/en_US.yml plugins/RaidEngine/lang/en_US.yml.bak
```

Keeping a copy or versioning the files makes it easier to restore in case of an error.

## Placeholder usage example

RaidEngine placeholders can be used directly in messages. Example:

```yml
placeholders:
  example: "<yellow>Clan %raidengine_f_name% [%raidengine_f_tag%]: DTR %raidengine_f_dtr% - %raidengine_f_state% - Online %raidengine_f_online% - Shield %raidengine_f_shield_timeleft%"
```
