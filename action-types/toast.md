# toast

**Action type**
<br>`[toast]`

**Description**
<br>Displays a toast popup notification (like the advancement popups).

## Syntax
[toast] <icon> <frame> <message>;[options]
```
#### Arguments
- **icon** — The material shown in the toast.
- **frame** — The toast frame style (`TASK`, `GOAL`, `CHALLENGE`).
- **message** — The text shown in the toast. Supports color codes and placeholders. Use `\n` to split the text into two lines.

## Options

Append after the arguments with a semicolon: `;key=value`

- `glow=<boolean>` — If set to true, gives the icon a glowing effect.
- `model-data=<value>` — Sets the CustomModelData value for the icon.

## Useful links
- [Toast Frame Types](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/advancement/Advancement.Frame.html)
- [Materials](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)

## Examples

### Simple task toast
```yaml
actions:
 - "[toast] DIAMOND TASK &aYou earned a reward!"
```

### Goal toast with two-line message
```yaml
actions:
 - "[toast] EMERALD GOAL &bQuest Complete!\n&7You finished Chapter 1"
```

### Toast with glowing custom icon
```yaml
actions:
 - "[toast] PLAYER_HEAD CHALLENGE &6Master Collector!;glow=true;model-data=12"
```
