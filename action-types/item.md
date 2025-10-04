# item

**Action type**
<br>`[item]`

**Description**
<br>Gives or takes a specified item from a player.
Supports two actions:
- **give** — Adds items to the player’s inventory.
- **take** — Removes items from the player’s inventory.

## Syntax
```
[item] <action> <material> <amount>
```
#### Arguments
- **action** — The action to perform (`give` or `take`).
- **material** — The material name (see Materials link below).
- **amount** — The number of items to give or take.

## Useful links
- [Materials](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)

## Examples

### Give the player 5 diamonds
```yaml
actions:
 - "[item] give DIAMOND 5"
```

### Take 1 emerald from the player
```yaml
actions:
 - "[item] take EMERALD 1"
```
