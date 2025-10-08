# message

**Action type**
<br>`[message]`

**Description**
<br>Sends a chat message to the player.
> [!NOTE]
> Supports both **Minecraft color codes** (`&a`, `&e`, etc.) and the **MiniMessage format** for advanced styling (click actions, hover text, gradients, hex colors, etc.).

## Syntax
```
[message] <text>
```
#### Arguments
- **text** — The message to display.

## Useful links
- [MiniMessage Viewer](https://webui.advntr.dev/)

## Examples

### Basic colored message
```yaml
actions:
 - "[message] &aWelcome to the server!"
```

### Simple MiniMessage formatting
```yaml
actions:
 - "[message] <gold>Victory! You defeated the boss!</gold>"
```

### Message with hover text
```yaml
actions:
 - "[message] <hover:show_text:'<gray>This is only shown on hover.'><yellow>Hover over this text!</yellow></hover>"
```

### Message with clickable URL
```yaml
actions:
 - "[message] <aqua><click:open_url:'https://example.com'>Visit our website</click></aqua>"
```

### Gradient styled announcement
```yaml
actions:
 - "[message] <gradient:#ff0000:#ffcc00>Server Restart in 5 Minutes!</gradient>"
```
