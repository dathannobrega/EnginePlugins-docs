# Guia de Clãs

## Jogadores

### Cargos
- **Recruta**: membro inicial com permissões básicas.
- **Moderador**: pode convidar ou expulsar recrutas e gerenciar warps.
- **Co-líder**: possui quase todos os poderes do líder, exceto transferir liderança.
- **Líder**: chefia o clã e define o prefixo exibido no chat.

### Banco
- Use `/f bank balance` para ver o saldo.
- Deposite com `/f bank deposit <quantia>` e saque com `/f bank withdraw <quantia>`.
- O saldo cobre custos de criação de clã, manutenção e posicionamento do núcleo.

### Warps
- Registre uma warp com `/f setwarp <nome> <senha>` (exige cargo apropriado).
- Apague com `/f delwarp <nome>`.
- Teleporte-se usando `/f warp <nome> <senha>`.
- A senha é necessária para criar e usar a warp; sem ela o teleporte falhará.
- Exemplo: `/f setwarp base 1234` e `/f warp base 1234`.

### Chat interno
- Ative ou desative com `/f chat`.
- Mensagens enviadas nesse modo são visíveis apenas aos membros do clã.

## Administradores

### Custos
- `clan.bank.create_cost`: custo para criar um clã (padrão **50 000**).
- `clan.bank.claim_place_cost`: custo para posicionar o núcleo e criar um claim (padrão **20 000**).
- `clan.bank.upkeep_per_claim`: taxa cobrada periodicamente por claim (padrão **1 000** a cada intervalo).

### Limites por nível
Defina limites no `config.yml` para escalonar o crescimento dos clãs:

| Nível | Máx. membros | Máx. claims | Máx. poder |
|------:|-------------:|------------:|-----------:|
| 1 | 5 | 1 | 100 |
| 2 | 10 | 2 | 200 |
| 3 | 15 | 3 | 300 |
| 4 | 20 | 4 | 400 |
| 5 | 25 | 5 | 500 |

### DTR-loss
- `clan.dtr.loss_on_death`: perda base de DTR por morte de membro (padrão **1.0**).
- `clan.dtr.loss_multiplier`: ajuste por mundo; exemplo:

```yaml
raidengine:
  clan:
    dtr:
      loss_multiplier:
        world: 1.0
        world_nether: 1.0
        world_the_end: 1.5
```

Cada multiplicador é aplicado ao valor base, permitindo tornar determinados mundos mais punitivos.
