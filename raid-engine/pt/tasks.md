# Tarefas Automáticas

## Enchimento de TNT

### Como funciona
- Preenche dispensers e droppers com TNT usando o banco do clã.
- É iniciado manualmente pelo comando `/f tnt fill <raio>` e processa alguns blocos por tick.

### Para administradores
#### Programação (cron)
- Não há agendamento automático.
- Caso deseje automatizar, agende o comando `/f tnt fill` via cron ou scheduler externo.
#### Parâmetros (`config.yml`)
- `raidengine.tnt.fill_max_radius`: raio máximo permitido.
- `raidengine.tnt.fill_base_tick_cost`: custo base em ticks por bloco preenchido.
#### Permissões
- `raidengine.clan.tnt` para permitir o comando de preenchimento.
- `raidadmin.admin` para execução via console ou automações.

## Manutenção de Claims

### Como funciona
- Cobra manutenção periódica proporcional ao número de claims.
- Se o saldo do clã for insuficiente, claims são removidos até a cobrança ser concluída.

### Para administradores
#### Programação (cron)
- Executada automaticamente a cada `clan.bank.upkeep_interval` ticks do servidor.
#### Parâmetros (`config.yml`)
- `raidengine.clan.bank.upkeep_interval`: intervalo entre cobranças.
- `raidengine.clan.bank.upkeep_per_claim`: custo base por claim.
- `raidengine.clan.bank.tax_rate`: multiplicador aplicado ao custo.
#### Permissões
- Administradores com `raidadmin.admin` podem disparar ou ajustar a tarefa manualmente conforme necessário.
