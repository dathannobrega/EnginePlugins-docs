# RaidEngine Placeholders

RaidEngine exposes placeholders through a single expansion identifier, typically `raidengine`. Use them with any PlaceholderAPI‑compatible plugin.

## Admins
- Format: `%raidengine_<key>%` for general values; `%raidengine_scoreboard_<key>%` for HUD/scoreboard stats.
- Examples:
  - `%raidengine_clan_name%`: player’s clan name
  - `%raidengine_scoreboard_player_kills%`: player kills for HUD

## Clan info (common)
- `%raidengine_scoreboard_clan_name%`: clan name
- `%raidengine_scoreboard_clan_level%`: clan level
- `%raidengine_scoreboard_clan_online%`: clan members online
- `%raidengine_scoreboard_power%`: player power
- `%raidengine_scoreboard_lands%`: number of clan claims

## Player stats (examples)
- `%raidengine_scoreboard_player_kills%`: kills
- `%raidengine_scoreboard_player_deaths%`: deaths
- `%raidengine_scoreboard_player_kd%` or `%raidengine_scoreboard_kd%`: K/D

## Territory and raid state
- `%raidengine_raid_state%`: `RAIDED`, `NORMAL`, or `NONE` outside claims
- `%raidengine_territory_name%`: owner clan or `Wilderness`
- `%raidengine_territory_raidable%`: `RAIDABLE` or `SAFE`
- `%raidengine_f_shield_timeleft%` / `%raidengine_shield_timeleft%`: remaining offline shield

## Economy and upkeep
- `%raidengine_f_balance%`: clan bank balance
- `%raidengine_upkeep_due%`: current upkeep amount
- `%raidengine_upkeep_next_cost%`: next upkeep cost

## Example (TAB)
```yaml
scoreboard:
  title: "&6RaidEngine"
  lines:
    - "&fClan: &a%raidengine_scoreboard_clan_name%"
    - "&fLevel: &a%raidengine_scoreboard_clan_level%"
    - "&fPower: &c%raidengine_scoreboard_power%"
    - "&fClaims: &c%raidengine_scoreboard_lands%"
    - "&fOnline: &c%raidengine_scoreboard_clan_online%"
    - "&fK/D: &c%raidengine_scoreboard_kd%"
```

## PlaceholderAPI integration
Ensure PlaceholderAPI is installed and the RaidEngine expansion is loaded:

```
/papi ecloud download raidengine
/papi reload
```
