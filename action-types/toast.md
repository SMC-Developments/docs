# toast

**Action type**
<br>`[toast]`

**Description**
<br>Displays a toast popup notification (like the advancement popups).

## Syntax
*BEFORE: `[toast] <icon>;<header>;<footer>;<frame>`
```
[toast] <icon> <frame> <header>;[footer]
```
#### Arguments
- **icon** — The material shown in the toast.
- **frame** — The toast frame style (`TASK`, `GOAL`, `CHALLENGE`).
- **header** — The main header text of the toast. Supports color codes and placeholders.
- **footer** *(optional)* — A subtitle below the header.

## Useful links
- [Toast Frame Types](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/advancement/Advancement.Frame.html)
- [Materials](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)

## Examples

### Simple task toast
```yaml
actions:
 - "[toast] DIAMOND TASK &aYou earned a reward!"
```

### Goal toast with header and footer
```yaml
actions:
 - "[toast] EMERALD GOAL &bQuest Complete!;&7You finished Chapter 1"
```
