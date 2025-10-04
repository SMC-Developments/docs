# summon

**Action type**
<br>`[summon]`

**Description**
<br>Summons one or more mobs near the player.

## Syntax
```
[summon] <mob> <amount> <radius> [display-name]
```
#### Arguments
- **mob** — The type of mob to summon.
- **amount** — The number of mobs to spawn.
- **radius** — The radius around the player where mobs can appear.
- **display-name** *(optional)* — The custom display name for the mob. Supports color codes and placeholders.

## Useful links
- [Entity Types](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/entity/EntityType.html)

## Examples

### Summon a single zombie next to the player
```yaml
actions:
 - "[summon] ZOMBIE 1 1 &aFriendly Zombie"
```

### Summon a group of skeletons in a 5-block radius
```yaml
actions:
 - "[summon] SKELETON 5 5 &cSkeleton Army"
```
