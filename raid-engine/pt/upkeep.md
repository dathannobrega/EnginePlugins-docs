# Manutenção de Claims

O RaidEngine cobra automaticamente uma taxa de manutenção de cada clã baseada na quantidade de claims que ele possui. O custo é calculado por claim e pode ser exibido com o placeholder `%raidengine_upkeep_next_cost%`.

Se o clã não possuir saldo suficiente no momento da cobrança, um claim será removido. Antes de cada remoção o líder é avisado no chat e a ação é registrada no histórico do clã através do `ClanActivityService`.

## Configurações de admin (`config.yml`)
- `raidengine.clan.bank.upkeep_interval`: intervalo (ticks) entre cobranças
- `raidengine.clan.bank.upkeep_per_claim`: custo base por claim
- `raidengine.clan.bank.tax_rate`: multiplicador aplicado ao custo base
