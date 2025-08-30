# GUI

## Color and Icon Guidelines

- Common icons are centralized in `MenuTheme`.
- **Back:** arrow (`Material.ARROW`) with text `gui.back`.
- **Confirm:** green wool (`Material.GREEN_WOOL`) with text `gui.confirm`.
- **Next:** arrow (`Material.ARROW`) with text `gui.next` to advance pages or levels.
- Use green for positive actions and red to cancel.

## For players

### ClaimConfirmMenu
- **How to open:** run `/claim` after previewing the area to be claimed.
- **Main actions:** confirm or cancel the creation of the claim.

### ClanBankConfirmMenu
- **How to open:** `/clan bank deposit <amount>` or `/clan bank withdraw <amount>`.
- **Main actions:** confirm deposits or withdrawals from the clan bank.

### ClanBankMenu
- **How to open:** "Bank" button inside `ClanInfoMenu`.
- **Main actions:** view balance, deposit, withdraw, and view recent transactions.

### ClanInfoMenu
- **How to open:** `/clan info`.
- **Main actions:** view clan balance and access member or permission menus.

### ClanMembersMenu
- **How to open:** "Members" button inside `ClanInfoMenu`.
- **Main actions:** see members and promote/demote roles.

### ClanPermissionsMenu
- **How to open:** "Permissions" button inside `ClanInfoMenu` (leader only inside the claim).
- **Main actions:** toggle flags for building, usage, chests, PVP, and other visitor access.

 

## For administrators
- Button texts, titles, and messages are customizable in `plugins/RaidEngine/lang/<locale>.yml`.
- Adjust default language and general options in `config.yml` (`raidengine.locale`).
- Upgrade costs and availability are configured in `config.yml` under `upgrades`.
 

## Usage tips
- Use the "Back" arrow item to quickly return to the previous menu.
- Set claim permissions carefully to prevent unwanted access to the territory.
