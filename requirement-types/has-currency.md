# has currency

**Requirement type**
<br>`has currency`

**Description**
<br>Checks if the player has at least the specified amount of a currency.  
> Requires the *SMC-Currency* plugin to be installed.

## Syntax
```yaml
type: has currency

# Sets the ID of the currency to check for.
id: TEXT

# Sets the amount of currency the player must have.
amount: #
```

## Examples

### Checks if the player has at least 100 coins
```yaml
requirements:
 - type: has currency
   id: coins
   amount: 100
```
