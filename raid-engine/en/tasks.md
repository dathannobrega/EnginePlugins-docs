# Automated Tasks

## TNT Fill

### How it works
- Fills dispensers/droppers with TNT using the clan bank funds.
- Trigger manually with `/f tnt fill <radius>`; it processes a few blocks per tick.

### Admin notes
#### Scheduling
- No built-in scheduler.
- If desired, schedule the command with a task scheduler or cron.
#### Parameters (`config.yml`)
- `raidengine.tnt.fill_max_radius`: maximum allowed radius.
- `raidengine.tnt.fill_base_tick_cost`: base tick cost per filled block.
#### Permissions
- Appropriate clan role to use the TNT command.
- `raidadmin.admin` for console/automation.

## Claim Upkeep

### How it works
- Periodically charges upkeep based on number of claims per clan.
- If the clan has insufficient balance, claims are removed until payment succeeds.

### Admin notes
#### Scheduling
- Runs automatically every `clan.bank.upkeep_interval` server ticks.
#### Parameters (`config.yml`)
- `raidengine.clan.bank.upkeep_interval`: interval between charges.
- `raidengine.clan.bank.upkeep_per_claim`: base cost per claim.
- `raidengine.clan.bank.tax_rate`: multiplier applied to the base cost.
#### Permissions
- Admins with `raidadmin.admin` can adjust configuration or trigger maintenance actions as needed.
