# Zonas

## Para jogadores

### Tipos de Zona (`ZoneType`)
- **SAFE** – área neutra sem PvP e com interações limitadas.
- **WAR** – área de guerra; claims desabilitados e recompensas maiores para missões de risco.
- **SPAWN** – região inicial do servidor com risco reduzido.
- **VAULT** – locais destinados a cofres e armazenamento.
- **FARM** – áreas de coleta e plantio controladas.

### Entrando em uma zona
- Use `/clan zone` para descobrir a zona atual.
- Zonas podem definir um `greeting`; ao entrar ou renascer dentro dela, o texto é enviado ao jogador.

## Para administradores

### Configuração de saudações
- Cada zona pode ter um campo `greeting` com códigos de cor usando `&`.
- A mensagem é exibida quando o jogador muda de mundo ou respawna dentro da zona.

### Registrar zonas via `config.yml`
Adicione a lista em `raidengine.zones`:

```yaml
raidengine:
  zones:
    - world: world_the_end
      type: WAR
      minX: -1000
      maxX: 1000
      minZ: -1000
      maxZ: 1000
      name: "End"
      greeting: "&cThe End é uma área de evento. Claims desabilitados."
```

Reinicie ou recarregue o plugin após salvar.

### Registrar zonas via comandos
1. Conceda a permissão `raidengine.clan.zone`.
2. No local desejado, execute `/clan zone <tipo> <raio>` para criar uma área quadrada ao seu redor.
3. O mesmo comando sem argumentos informa o nome e o `greeting` da zona atual.
4. Para personalizar `name` ou `greeting`, edite o `config.yml` após a criação.
