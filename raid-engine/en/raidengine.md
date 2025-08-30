# RaidEngine
![Engine Plugins - Banner](../assets/images/banners/banner-home.png)
## Installation
1. Download the RaidEngine `.jar` file.
2. Place it in the `plugins` folder of your Spigot or Paper server.
3. Restart the server and check if the plugin has loaded correctly.

## Core Overview
RaidEngine introduces clan, territory, and war mechanics. The goal is to compete for areas of the map and strengthen your clan to dominate the server.

## Clan Progression
- Obtain resources to gain experience and level up.
- Level up to unlock upgrades and bonuses for members.

## Tips
- Cooperate with your clanmates to evolve faster.
- Use the map to plan attacks and defenses.

## Game Flows
### Create Clan
1. Use `/clan create <name>` to found a new clan.
2. Invite friends with `/clan invite <player>`.
3. Set the base and organize member roles.

### Claim Territory
1. Go to the desired area.
2. Execute `/claim` to confirm the selected area for your clan.
3. Protect the region against invaders.

### War Windows
- Raids only happen during configured time windows.
- Leaders declare or accept wars; check with your admins for local rules.

## Administrators

### Dependencies
- Recent Spigot or Paper server.
- Compatible economy plugin (e.g., Vault).
- Configured database, if necessary, for persistence.

### Global Permissions
- `raidengine.admin` for full access (group defined in `plugin.yml`).
- `raidadmin.admin` to use the admin command.

### Main Commands
- `/raidadmin reload` to reload configuration and messages.
- `/raidadmin give <player> claim_core <amount>` to grant Claim Cores.
- `/raidadmin world <enable|disable|list>` manage worlds where claims apply.

### General Guides
- [Database and backups](data.md)
- [Scoreboard](scoreboard.md)
- [Messages and languages](messages.md)

