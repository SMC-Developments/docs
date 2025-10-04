# exp

**Action type**
<br>`[exp]`

**Description**
<br>Gives or takes experience from a player.
Supports two actions:
- **give** — Adds experience to the player.
- **take** — Removes experience from the player.

## Syntax
```
[exp] <action> <amount>;[options]
```
#### Arguments
- **action** — The action to perform (`give` or `take`).
- **amount** — The amount of experience to give or take.

## Options
Append after the arguments with a semicolon: `;key=value`
- `level=boolean` — If set to true, the amount will be counted as levels.

## Examples

### Take 100 experience points
```yaml
actions:
 - "[exp] take 100"
```

### Reward multiple types of experience
```yaml
actions:
 - "[exp] give 10"
 - "[exp] give 3;level=true"
```
