# War and Raids

## Flow
1. Leaders declare or accept wars according to your server’s rules and schedule.
2. Raids can only progress between `raid.start_time` and `raid.end_time`.
3. TNT explosions near the enemy core deal `raid.tnt.damage` to its HP during valid raid time.
4. At 0 HP, the claim enters the **RAIDED** state for `raid.raided_duration_minutes`, temporarily relaxing protections.

## Players
### Attacking
- Coordinate with your clan, bring TNT, and attack during the allowed window.
- Focus the enemy core to drain HP faster.

### Defending
- Keep defenders online; if fully offline, the enemy may be blocked by the offline shield depending on settings.
- Fortify the area around the core and repair damage promptly.

### Alerts
- When a core is attacked, members receive clear alerts (chat/bossbar/sound).

## Administrators
### Key settings (`config.yml`)
- `raid.start_time` / `raid.end_time`: raid window.
- `raid.tnt.damage`: damage per TNT explosion to the core.
- `raid.raided_duration_minutes`: RAIDED duration after core HP reaches 0.
- `war.grace_until`: optional global grace date/time to block new wars.
- `war.offline_shield.enabled`: enable offline shield.
- `war.offline_shield.min_online_defenders`: online defenders to prevent shield.
- `war.offline_shield.cooldown_minutes`: cooldown after using the shield.

### Costs and economy
- Tune costs in `clan.bank` (e.g., claim placement, upkeep) to balance progression.
