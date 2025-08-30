# Claim Upkeep

RaidEngine automatically charges upkeep to each clan based on the number of claims it owns. The cost is calculated per claim and can be shown with `%raidengine_upkeep_next_cost%`.

If the clan doesn’t have enough balance when charged, a claim is removed. Leaders are warned before each removal and the action is recorded in the clan history.

## Admin settings (`config.yml`)
- `raidengine.clan.bank.upkeep_interval`: tick interval between charges
- `raidengine.clan.bank.upkeep_per_claim`: base cost per claim
- `raidengine.clan.bank.tax_rate`: multiplier applied to the base cost
