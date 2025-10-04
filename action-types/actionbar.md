# actionbar

**Action type**
<br>`[actionbar]`

**Description**
<br>Sends a message to the player’s actionbar (the text area above the hotbar).

## Syntax
```
[actionbar] <duration> <text>
```
#### Arguments
- **duration** — How long the actionbar message should stay visible (in ticks).
- **text** — The message to display. Supports color codes and placeholders.

## Examples

### Show a short actionbar message
```yaml
actions:
 - "[actionbar] 40 &aAbility Ready!"
```

### Show player stats
```yaml
actions:
 - "[actionbar] 60 &aHP: &c%player_health%&7/&c%player_max_health%"
```
