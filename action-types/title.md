# title

**Action type**
<br>`[title]`

**Description**
<br>Displays a title and subtitle on the player’s screen.

## Syntax
```
[title] <fade-in> <stay-time> <fade-out> <title>;[subtitle]
```
#### Arguments
- **fade-in** — Time (in ticks) for the title to fade in.
- **stay-time** — Time (in ticks) for the title to remain visible.
- **fade-out** — Time (in ticks) for the title to fade out.
- **title** — The main title text. Supports color codes and placeholders.
- **subtitle** *(optional)* — The subtitle text shown below the title. Supports color codes and placeholders.

## Examples

### Welcome a player with a title
```yaml
actions:
 - "[title] 10 60 10 &aWelcome!;&7Enjoy your stay"
```

### Show an alert with no subtitle
```yaml
actions:
 - "[title] 5 40 5 &cWarning!"
```
