# effect

**Action type**
<br>`[effect]`

**Description**
<br>Applies a potion effect to the player.

## Syntax
```
[effect] <type> <amplifier> <duration>
```
#### Arguments
- **type** — The potion effect type.  
- **amplifier** — The effect strength (0 = level 1, 1 = level 2, etc.).  
- **duration** — The duration of the effect in ticks (20 ticks = 1 second). 

## Useful links
- [Potion Effect Types](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/potion/PotionEffectType.html)

## Examples

### Give the player Speed II for 10 seconds
```yaml
actions:
 - "[effect] SPEED 1 200"
```

### Apply Strength I for 30 seconds
```yaml
actions:
 - "[effect] INCREASE_DAMAGE 0 600"
```
