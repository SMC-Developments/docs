## Gui Menu
GUI menus let you create fully customizable inventory interfaces for your players.  
You can set titles, define layouts, attach conditions, assign open commands, and add items with actions.  
Menus are highly flexible and can be combined with conditions and actions to create advanced interactive systems.

### Syntax
```yaml
gui-menu:
  title: "TEXT"
  rows: #
  inventory-type: "TEXT"
  conditions: CONDITIONS
  open-commands: COMMANDS
  items: ITEMS
  extensions: EXTENSIONS
```

### title
```yaml
title: "TEXT"
```
Sets the menu title that is shown at the top of the GUI.
<br>Supports color and formatting codes as well as PlaceholderAPI placeholders.

### rows
```yaml
rows: #
```
> *Supported values:* `1`, `2`, `3`, `4`, `5`, `6`\
> *Default value:* `6`

Sets the number of rows for the GUI menu.

### inventory type
```yaml
inventory-type: "TEXT"
```
> *Supported values:* `ANVIL`, `BARREL`, `BEACON`, `BLAST_FURNACE`, `BREWING`, `CARTOGRAPHY`, `DISPENSER`, `DROPPER`, `ENCHANTING`, `ENDER_CHEST`, `FURNACE`, `HOPPER`, `LOOM`, `PLAYER`, `SHULKER_BOX`, `SMOKER`, `WORKBENCH`\
> *Default value:* `CHEST`

Sets the type of inventory the menu will use.

### conditions
```yaml
conditions: CONDITIONS
```
Sets the conditions the player must meet to open the GUI menu.
<br>Check the [Conditions](conditions.md) section for more information.

### open commands
```yaml
open-commands: COMMANDS
```
Sets the commands that will open the GUI menu. It can only be a single word.
<br>Check the [Commands](commands.md) section for more information.

### items
```yaml
items: ITEMS
```
Sets the items that appear in the GUI menu.
<br>Check the [Items](https://github.com/VinceSMC/SMC-Developments/blob/284febd0ab3c6d5c2b839fa91d4bc69aae38247a/documentation/gui-menus/items.md) section for more information.

### extensions
```yaml
extensions: EXTENSIONS
```
Sets the extensions linked to this GUI menu.
Extensions allow you to add extra lore or override click actions on existing items.
<br>Check the [Extensions](https://github.com/VinceSMC/SMC-Developments/blob/284febd0ab3c6d5c2b839fa91d4bc69aae38247a/documentation/gui-menus/extensions.md) section for more information.


