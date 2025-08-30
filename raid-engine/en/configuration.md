# Configuration

## Administrators

### `config.yml`
The file defines the plugin's global parameters and is generated in the data folder (`plugins/RaidEngine`). Adjust in it:

- `raidengine.locale`: default language code (matches a file in `plugins/RaidEngine/lang`, e.g., `en_US`).
- `raidengine.worlds_enabled`: worlds where claims are allowed.
- `raidengine.database`: type (`sqlite` or `mysql`), host, user, and password.
- Other sections like `claim`, `clan`, and `upgrades` for specific rules.
- Raid and war timings are under `raid.*` and `war.*`.

### Profiles (deprecated)
Older builds supported configuration profiles. The current version consolidates settings in a single `config.yml`. The `raidengine.profile` key is ignored.

### Language files (`plugins/RaidEngine/lang/*.yml`)
Customize all texts by editing files like `en_US.yml` or `pt_BR.yml` inside `plugins/RaidEngine/lang`. Bukkit/MiniMessage colors and placeholders like `%amount%` are supported.

The texts accept Bukkit/MiniMessage colors and placeholders like `%amount%`. See the [messages guide](messages.md) for details on structure, colors, and how to add new languages.

### SQL Connection (`HikariConfigFactory`)
The class creates the `HikariConfig` based on `config.yml`, allowing the use of SQLite or connecting to a MySQL server. Ensure that `raidengine.database` has the correct data for the chosen type.

### Migrations (`SchemaMigrator`)
During startup, the plugin converts the SQL schema file to the format expected by the defined database. The `SchemaMigrator` changes, for example, `AUTOINCREMENT` to `AUTO_INCREMENT` when using MySQL.

## Players
Custom messages can be translated according to your language. Ask admins to adjust the files in `plugins/RaidEngine/lang/` or change the `raidengine.locale` in `config.yml`.
