## Conditions
Conditions are checks that must be met before an action or feature can be used.
They can validate things like permissions, items, or placeholders. You can combine multiple requirements and control what happens if they are met or not.

### Syntax
```yaml
conditions:
  # Sets the actions to run when all requirements are met.
  success-actions: ACTIONS

  # Sets the actions to run when the requirements are not met.
  deny-actions: ACTIONS

  # Sets how many requirements from the list must be fulfilled.
  # If not set, all listed requirements will be required.
  minimum-requirements: 1

  # Lists all the requirements that will be checked.
  requirements:
   - type: has permission
     permission: rank.vip
```

### Requirement types

| # | Type            | Description                                                                 |
|---|-----------------|-----------------------------------------------------------------------------|
| 1 | [`has item`](requirement-types/has-item.md) | Checks if the player has the specified item in their inventory. |
| 2 | [`has permission`](requirement-types/has-permission.md) | Checks if the player has the specified permission. |
| 3 | [`has currency`](requirement-types/has-currency.md) | Checks if the player has at least the specified amount of a currency. |
| 4 | [`comparator`](requirement-types/comparator.md) | Compares an input with an output using operators like `==`, `>=`, etc. |
| 5 | [`at location`](requirement-types/at-location.md) | Checks whether the player is at the required location. |

ㅤ
## Examples

### Restrict access to OP players
```yaml
conditions:
  deny-actions:
   - "[message] &cYou need to be OP to use this feature!"
  requirements:
   - type: "=="
     input: "%player_is_op%"
     output: "yes"
```

### Require at least 100 coins
```yaml
conditions:
  deny-actions:
   - "[message] &cYou don't have enough coins!"
  requirements:
   - type: has currency
     id: coins
     amount: 100
```


