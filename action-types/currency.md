# currency

**Action type**
<br>`[currency]`

**Description**
<br>Gives or takes a certain amount of a currency from a player. Supports two actions:
- **give** — Adds the specified currency to the player.
- **take** — Removes the specified currency from the player.
> Requires the *SMC-Currency* plugin to be installed.

## Syntax
```
[currency] <action> <currency> <amount>
```
#### Arguments
- **action** — The action to perform (`give` or `take`).
- **currency** — The currency ID (as defined in the SMC-Currency plugin).
- **amount** — The amount of currency to give or take.

## Examples

### Take 5 gems from a player
```yaml
actions:
 - "[currency] take gems 5"
```

### Reward with coins and gems together
```yaml
actions:
 - "[currency] give coins 25"
 - "[currency] give gems 3"
```
