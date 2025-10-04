# bossbar

**Action type**
<br>`[bossbar]`

**Description**
<br>Displays a temporary bossbar message at the top of the player’s screen.

## Syntax
```
[bossbar] <style> <progress> <color> <duration> <text>
```
#### Arguments
- **style** — The bar’s visual style (segments).
- **progress** — The bar’s progress (from `0` to `100`).
- **color** — The bar’s color.
- **duration** — How long the bossbar should stay visible (in ticks).
- **text** — The message displayed in the bossbar. Supports color codes and placeholders.

## Useful links
- [BossBar Styles](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/boss/BarStyle.html)  
- [BossBar Colors](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/boss/BarColor.html)  

## Examples

### Simple red bossbar at half progress
```yaml
actions:
 - "[bossbar] SOLID 50 RED 100 &cBoss Incoming!"
```

### Green segmented bossbar
```yaml
actions:
 - "[bossbar] SEGMENTED_10 100 GREEN 200 &aQuest Completed!"
```
