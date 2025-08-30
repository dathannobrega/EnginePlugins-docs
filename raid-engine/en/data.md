# Database and backups

## Database options
- **SQLite**: default; stores data locally in `plugins/RaidEngine/raidengine.db`. Simple to configure and ideal for small servers.
- **MySQL**: requires an external server. Configure `host`, `port`, `database`, `user`, and `password` in `config.yml`. Recommended for networks or environments with multiple instances.

## Migrations
- The plugin runs SQL migrations to create/upgrade the schema.
- Migrations adapt SQL to the selected database when needed (e.g., SQLite vs MySQL).
- Before updating the plugin, make a backup to be safe.

## Backup procedures
### Backup
1. Stop the server or block new connections.
2. For **SQLite**, copy `raidengine.db`. For **MySQL**, use `mysqldump`.
3. Store the files in a safe and versioned location.

### Restoration
1. Stop the server.
2. Replace `raidengine.db` with the backup or import the `.sql` file into MySQL.
3. Start the server and check if the data has been loaded correctly.

## Maintenance routines and best practices
- Schedule automatic backups (daily or weekly) and keep multiple versions.
- Periodically test the restoration in a staging environment.
- Monitor disk space and the integrity of database files.
- Keep the MySQL server updated and restrict access to credentials.
- Use protection against power outages to prevent data corruption.
- Perform a full backup before updating the plugin or running manual migrations.
