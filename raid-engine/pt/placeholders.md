# Placeholders do RaidEngine

Todos os placeholders são fornecidos por uma única expansão com o identificador `raidengine`.
Para estatísticas exibidas em HUDs/placares externos, utilize parâmetros com o prefixo `scoreboard_`.

Qualquer plugin compatível com PlaceholderAPI (como TAB, FeatherBoard, DeluxeMenus)
pode usar esses placeholders para montar scoreboards personalizados.

## Administradores

### Formato

Os placeholders seguem o padrão `%raidengine_<chave>%`.
Para estatísticas de HUD e placar, utilize `%raidengine_scoreboard_<chave>%`.

Exemplos:

* `%raidengine_clan_name%` — retorna o nome do clã do jogador.
* `%raidengine_scoreboard_player_kills%` — mostra os abates do jogador na HUD.

### Informações do clã

| Placeholder | Descrição |
|-------------|-----------|
| `%raidengine_scoreboard_clan_name%` | Nome do clã do jogador. |
| `%raidengine_scoreboard_clan_level%` | Nível do clã do jogador. |
| `%raidengine_scoreboard_clan_online%` | Membros do clã online. |
| `%raidengine_scoreboard_power%` | Poder atual do jogador. |
| `%raidengine_scoreboard_lands%` | Número de claims do clã. |

### Estatísticas do jogador

| Placeholder | Descrição |
|-------------|-----------|
| `%raidengine_scoreboard_player_kills%` | Abates do jogador. |
| `%raidengine_scoreboard_player_deaths%` | Mortes do jogador. |
| `%raidengine_scoreboard_player_kd%` | Relação de abates/mortes do jogador. |
| `%raidengine_scoreboard_kd%` | Relação de abates/mortes do jogador. |
| `%raidengine_scoreboard_kd%` | Relação de abates/mortes do jogador. |

### Placeholders adicionais

| Placeholder | Saída esperada e uso |
|-------------|----------------------|
| `%raidengine_f_power%` | Poder total do clã do jogador. Use para mostrar a força coletiva do clã. |
| `%raidengine_f_max_power%` | Poder máximo que o clã do jogador pode alcançar. |
| `%raidengine_f_claims%` | Total de terrenos reivindicados pelo clã. Útil em placares ou menus de informação. |
| `%raidengine_f_member_count%` | Quantidade de membros no clã do jogador. |
| `%raidengine_f_role%` | Cargo do jogador no clã, como `LEADER`, `MEMBER` ou outros. |
| `%raidengine_f_balance%` | Saldo do banco do clã do jogador, formatado com duas casas decimais. |
| `%raidengine_f_name%` | Nome do clã do jogador. |
| `%raidengine_f_tag%` | Prefixo/tag do clã do jogador. |
| `%raidengine_f_dtr%` | DTR (Deaths Till Raidable) atual do clã. |
| `%raidengine_f_state%` | Estado de raid do clã do jogador: `RAIDABLE` ou `SAFE`. |
| `%raidengine_f_online%` | Membros do clã atualmente online. |
| `%raidengine_f_shield_timeleft%` | Tempo restante de proteção offline do clã, em minutos e segundos. |
| `%raidengine_raid_state%` | Estado do terreno onde o jogador está: `RAIDED`, `NORMAL` ou `NONE` fora de claims. Ideal para HUDs de raid. |
| `%raidengine_territory_raidable%` | Indica se o território atual pode ser raidado: `RAIDABLE` quando pode ser atacado, `SAFE` caso contrário. |
| `%raidengine_territory_name%` | Nome do clã que possui o território atual; mostra `Wilderness` fora de claims. |
| `%raidengine_shield_timeleft%` | Tempo restante de proteção offline do clã, em minutos e segundos. Exiba para avisar quando a proteção acabará. |
| `%raidengine_upkeep_due%` | Custo atual de manutenção dos claims do clã. Pode ser usado para alertar líderes sobre pagamentos. |
| `%raidengine_upkeep_next_cost%` | Próximo custo de manutenção dos claims do clã. Útil para HUDs e comandos. |


### Exemplo de scoreboard (TAB)

```yaml
scoreboard:
  title: "&6RaidEngine"
  lines:
    - "&fClã: &a%raidengine_scoreboard_clan_name%"
    - "&fNível: &a%raidengine_scoreboard_clan_level%"
    - "&fPoder: &c%raidengine_scoreboard_power%"
    - "&fClaims: &c%raidengine_scoreboard_lands%"
    - "&fMembros: &c%raidengine_scoreboard_clan_online%"
    - "&fK/D: &c%raidengine_scoreboard_kd%"
```

### Uso em plugins externos

Os placeholders estão registrados no PlaceholderAPI. Qualquer plugin compatível pode usá-los. Exemplo com DeluxeMenus:

```yaml
menu:
  items:
    power:
      text: "Poder: %raidengine_scoreboard_power%"

### Integração com PlaceholderAPI

Garanta que o PlaceholderAPI esteja instalado e a expansão `raidengine` carregada:

```
/papi ecloud download raidengine
/papi reload
```
```

### Integração com PlaceholderAPI

Certifique-se de que o PlaceholderAPI esteja instalado e que a expansão `raidengine` esteja carregada:

```
/papi ecloud download raidengine
/papi reload
```
