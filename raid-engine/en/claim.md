# Claim System

## For players

### Crafting
- Obtain the **Claim Core** via the server recipe (lodestone + obsidian + netherite) or ask an admin to grant one with `/raidadmin give`.

### Preview
- Try placing the core to preview the area. If it’s valid (no collisions and meets minimum relative height), you’ll see particles and a bossbar.
- Confirm with `/claim` to create the territory.

### Confirmation
- Use `/claim` to open the confirmation menu. On confirm, the clan bank is charged (`clan.bank.claim_place_cost`).

### Upgrades
- The radius and core HP scale with configuration and clan progression.

### Defense tips
- Position the core in a protected location, preferably in the center of the base, to make attacks difficult.
- Keep free space around it to prevent enemies from using the terrain as cover.
- Take advantage of the `claim.anti_cover` feature to prevent constructions that over-protect the core.

### Common errors when placing the core
- Trying to place the core too low or too high in relation to the terrain, violating `claim.min_relative_height`.
- Placing the core adjacent to another existing claim.
- Not having enough money in the clan bank for the placement cost.
- Forgetting to confirm with `/claim` after the preview.

## For administrators

### Configuration keys (`config.yml`)
- `worlds_enabled`: worlds where the claim system is valid.
- `preview.particles` and `preview.bossbar`: control preview effects.
- `claim.min_relative_height` and `claim.anti_cover`: core placement rules.
- `claim.levels`: defines radius and HP per level.
- `claim.core.base_hp`: initial core health.
- `clan.max_claims_by_level`: claim limit per clan level.
- `clan.bank.claim_place_cost`: cost to place the core.

### Messages
- Customize titles, confirmation texts, and other notices in the language files under `plugins/RaidEngine/lang/` (for example, `en_US.yml`).

### Permissions
- The `/claim` command is available to everyone. Administrative commands, such as `/raidadmin`, require specific nodes (`raidadmin.admin`, `raidadmin.give`, etc.) as defined in `plugin.yml`.
