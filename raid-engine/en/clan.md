# Clan Guide

## Players

### Roles
- **Recruit**: initial member with basic permissions.
- **Moderator**: can invite or kick recruits and manage warps.
- **Co-leader**: has almost all the leader's powers, except transferring leadership.
- **Leader**: heads the clan and sets the prefix displayed in the chat.

### Bank
- Use `/f bank balance` to see the balance.
- Deposit with `/f bank deposit <amount>` and withdraw with `/f bank withdraw <amount>`.
- The balance covers the costs of creating a clan, maintenance, and placing the core.

### Warps
- Register a warp with `/f setwarp <name> <password>` (requires appropriate role).
- Delete with `/f delwarp <name>`.
- Teleport using `/f warp <name> <password>`.
- The password is required to create and use the warp; without it, the teleport will fail.
- Example: `/f setwarp base 1234` and `/f warp base 1234`.

### Internal chat
- Enable or disable with `/f chat`.
- Messages sent in this mode are visible only to clan members.

## Administrators

### Costs
- `clan.bank.create_cost`: cost to create a clan (default **50,000**).
- `clan.bank.claim_place_cost`: cost to place the core and create a claim (default **20,000**).
- `clan.bank.upkeep_per_claim`: fee charged periodically per claim (default **1,000** per interval).

### Limits per level
Define limits in `config.yml` to scale the growth of clans:

| Level | Max. members | Max. claims | Max. power |
|------:|-------------:|------------:|-----------:|
| 1 | 5 | 1 | 100 |
| 2 | 10 | 2 | 200 |
| 3 | 15 | 3 | 300 |
| 4 | 20 | 4 | 400 |
| 5 | 25 | 5 | 500 |

### DTR-loss
- `clan.dtr.loss_on_death`: base DTR loss per member death (default **1.0**).
- `clan.dtr.loss_multiplier`: adjustment per world; example:

```yaml
raidengine:
  clan:
    dtr:
      loss_multiplier:
        world: 1.0
        world_nether: 1.0
        world_the_end: 1.5
```

Each multiplier is applied to the base value, allowing certain worlds to be more punitive.
