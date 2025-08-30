# LuckPerms

## For players
- If a RaidEngine command doesn't work, the server is checking for a `raidengine.*` node that your group doesn't have yet.
- Contact an administrator to have the permission granted.

## For administrators
### Granting access
Use [LuckPerms](https://luckperms.net/) to grant specific permissions to players or groups.

```bash
/lp user Steve permission set raidengine.claim.place true
/lp group members permission set raidengine.clan.create true
```

Tip: keep it simple by assigning the predefined groups from `plugin.yml`:

```bash
/lp group default permission set raidengine.user true
/lp group admin permission set raidengine.admin true
```

### Main nodes
| Permission | Description | Default |
|---|---|---|
| `raidengine.user` | Default user group | `true` |
| `raidengine.admin` | Admin group (includes user and admin nodes) | `op` |
| `raidadmin.admin` | Access to `/raidadmin` command | `op` |
| `raidadmin.reload` | Reload configuration/messages | `op` |
| `raidadmin.give` | Give Claim Cores and tools | `op` |
| `raidadmin.world` | Enable/disable/list enabled worlds | `op` |
| `raidadmin.profile` | Legacy profile toggle (deprecated) | `op` |
| `raidengine.clan.admin.*` | Clan admin tools | `op` |
| `raidengine.antiglitch.bypass` | Bypass anti‑glitch checks | `op` |

### Group examples
```bash
/lp group default permission set raidengine.user true
/lp group admin permission set raidengine.admin true
```
