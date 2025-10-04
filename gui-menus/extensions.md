# Extensions
Extensions allow you to extend or modify existing GUI menu items.
<br>They can add variable lores that are only visible when conditions are met, and they can also override the click actions of targeted items.

### Syntax
```yaml
extensions:
  extension-id:
    lore: LIST
```
*Note: Always use a unique extension-id to prevent conflicts.*

### lore
```yaml
lore:
 - "TEXT"
 - "TEXT"
```
Sets the item’s lore (the text shown under the item’s name). Supports placeholders and color/format codes.

### lore index
```yaml
lore-index: #
```
Sets the exact lore line where the extension should appear on the targeted menu item.
<br>If not specified, the lore will be added to the last row.

### priority
```yaml
priority: #
```
Sets the extension’s priority number.
<br>If multiple extensions target the same item and the player meets more than one extension’s conditions, the extension with the highest priority will be displayed first. The highest priority is `0`.

### parent items
```yaml
parent-items:
 - item-id_1
 - item-id_2
```
Targets one or more GUI menu items by their item-id.

### click actions
```yaml
left-click-actions: ACTIONS
shift-left-click-actions: ACTIONS
right-click-actions: ACTIONS
shift-right-click-actions: ACTIONS
click-actions: ACTIONS
```
Sets the actions to run when the item is clicked. These override the click actions of the targeted item.
<br>Actions execute from top to bottom in the list.
<br>Check the [Actions](https://github.com/VinceSMC/SMC-Developments/blob/f5a97c218bf83512aa6d5232cb35e18444c6d88d/documentation/actions.md) section for more information.

### conditions
```yaml
conditions: CONDITIONS
```
Sets the conditions the player must meet to view the extension.
<br>Check the [Conditions](https://github.com/VinceSMC/SMC-Developments/blob/main/documentation/conditions.md) section for more information.

## Examples

### Simple extension with lore and a click override
```yaml
items:
  example-item:
    material: EMERALD
    slot: 13
    display-name: "&aExample"
    lore:
     - "&7This is the base item"

extensions:
  extra-info:
    lore:
     - "&bExtra lore visible if you are OP"
    parent-items:
     - example-item
    conditions:
      requirements:
       - type: "=="
         input: "%player_is_op%"
         output: "yes"
    left-click-actions:
     - "[message] &bThis is an extension action!"
```
