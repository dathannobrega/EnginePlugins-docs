# Scoreboard

RaidEngine doesn’t ship a built‑in scoreboard. Instead, it exposes placeholders via PlaceholderAPI so you can use any scoreboard/HUD plugin (e.g., TAB, FeatherBoard, DeluxeMenus overlays).

## For players
- Your server may show a HUD with clan info using RaidEngine placeholders.
- If the HUD gets in the way, most scoreboard plugins provide a toggle command.

## For administrators
### Setup
1. Install PlaceholderAPI and your preferred scoreboard plugin.
2. Install the RaidEngine expansion, if provided, and reload placeholders:
   - `/papi ecloud download raidengine`
   - `/papi reload`

### Useful placeholders
- `%raidengine_scoreboard_clan_name%`: player’s clan name
- `%raidengine_scoreboard_clan_level%`: clan level
- `%raidengine_scoreboard_clan_online%`: online clan members
- `%raidengine_scoreboard_power%`: player power
- `%raidengine_scoreboard_lands%`: clan claims
- `%raidengine_scoreboard_kd%`: player K/D
- `%raidengine_raid_state%`: current territory state

See Integrations → Placeholders for more options.

### Example (TAB)
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

### Tips
- Keep lines concise and avoid overly expensive placeholders.
-.Reload your scoreboard plugin during low activity if you make big changes.
