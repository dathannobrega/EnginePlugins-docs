# LuckPerms

## Para jogadores
- Se um comando do RaidEngine não funcionar, o servidor está verificando um nó `raidengine.*` que seu grupo ainda não possui.
- Entre em contato com um administrador para que a permissão seja concedida.

## Para administradores
### Concedendo acesso
Use o [LuckPerms](https://luckperms.net/) para liberar permissões específicas para jogadores ou grupos.

```bash
/lp user Steve permission set raidengine.claim.place true
/lp group membros permission set raidengine.clan.create true
```

Dica: simplifique usando os grupos predefinidos do `plugin.yml`:

```bash
/lp group default permission set raidengine.user true
/lp group admin permission set raidengine.admin true
```

### Nós principais
| Permissão | Descrição | Padrão |
|-----------|-----------|--------|
| `raidengine.user` | Grupo padrão de usuário | `true` |
| `raidengine.admin` | Grupo admin (inclui nós de admin e usuário) | `op` |
| `raidadmin.admin` | Acesso ao comando `/raidadmin` | `op` |
| `raidadmin.reload` | Recarrega configurações/mensagens | `op` |
| `raidadmin.give` | Entrega Núcleos de Claim e ferramentas | `op` |
| `raidadmin.world` | Ativa/desativa/lista mundos habilitados | `op` |
| `raidadmin.profile` | Alterna perfil legado (descontinuado) | `op` |
| `raidengine.clan.admin.*` | Ferramentas administrativas de clã | `op` |
| `raidengine.antiglitch.bypass` | Ignora checagens anti‑glitch | `op` |

### Exemplos de grupos
```bash
/lp group default permission set raidengine.user true
/lp group admin permission set raidengine.admin true
```
