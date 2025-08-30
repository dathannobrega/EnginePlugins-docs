# Scoreboard

O RaidEngine não inclui um placar próprio. Em vez disso, expõe placeholders via PlaceholderAPI para que você use qualquer plugin de HUD/placar (TAB, FeatherBoard, DeluxeMenus etc.).

## Para jogadores
- Seu servidor pode exibir uma HUD com informações do clã usando placeholders do RaidEngine.
- Se a HUD atrapalhar, a maioria dos plugins oferece comando para alternar/ocultar.

## Para administradores
### Setup
1. Instale o PlaceholderAPI e o plugin de placar de sua preferência.
2. Instale a expansão do RaidEngine (se fornecida) e recarregue os placeholders:
   - `/papi ecloud download raidengine`
   - `/papi reload`

### Placeholders úteis
- `%raidengine_scoreboard_clan_name%`: nome do clã do jogador
- `%raidengine_scoreboard_clan_level%`: nível do clã
- `%raidengine_scoreboard_clan_online%`: membros online do clã
- `%raidengine_scoreboard_power%`: poder do jogador
- `%raidengine_scoreboard_lands%`: claims do clã
- `%raidengine_scoreboard_kd%`: K/D do jogador
- `%raidengine_raid_state%`: estado do território atual

Veja Integrações → Placeholders para mais opções.

### Exemplo (TAB)
```yaml
scoreboard:
  title: "&6RaidEngine"
  lines:
    - "&fClã: &a%raidengine_scoreboard_clan_name%"
    - "&fNível: &a%raidengine_scoreboard_clan_level%"
    - "&fPoder: &c%raidengine_scoreboard_power%"
    - "&fClaims: &c%raidengine_scoreboard_lands%"
    - "&fOnline: &c%raidengine_scoreboard_clan_online%"
    - "&fK/D: &c%raidengine_scoreboard_kd%"
```

### Dicas
- Mantenha as linhas concisas e evite placeholders muito pesados.
- Recarregue seu plugin de placar em horários de menor movimento se fizer mudanças grandes.
