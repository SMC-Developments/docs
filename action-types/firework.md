# firework

**Action type**
<br>`[firework]`

**Description**
<br>Launches a firework effect at the player’s location.

## Syntax
```
[firework] <type> <power> <y-offset> <color1>,<color2>,<color3>...
```
#### Arguments
- **type** — The firework’s explosion shape.
- **power** — Sets how long the firework travels before exploding.
- **y-offset** — Vertical offset from the player’s position (e.g. `1.5` to spawn just above the head).
- **colors** — A comma-separated list of colors for the explosion. Supports one or more colors.

> The flight duration is calculated with the formula `(power + 1) * 10 + random(0–5) + random(0–6)` ticks. When **power** is set to `0` it will explode after 2 ticks, `1` gives a short flight of about 1.8 to 2.5 seconds, `2` produces a medium flight of about 2.8 to 3.5 seconds, and `3` reaches a long flight of about 3.8 to 4.5 seconds. The valid range is 0–128. 

## Useful links
- [Firework Types](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/FireworkEffect.Type.html)
- [Colors](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Color.html)

## Examples

### Launch a red ball firework
```yaml
actions:
 - "[firework] BALL 0 0.5 RED"
```

### Launch a creeper-shaped firework with yellow and green colors
```yaml
actions:
 - "[firework] CREEPER 1 3.0 YELLOW,GREEN"
```

### Launch a burst firework with a rainbow of colors
```yaml
actions:
 - "[firework] BURST 2 2.0 RED,ORANGE,YELLOW,GREEN,BLUE,PURPLE"
```
