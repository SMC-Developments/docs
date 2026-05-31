# block below

**Requirement type**
<br>`block below`

**Description**
<br>Checks if the block below the player matches the specified material.

## Syntax
```yaml
type: block below

# Sets the block material that must be found below the player.
block: MATERIAL

# Sets the block materials that may be found below the player.
# Use this when multiple materials should be accepted.
blocks:
- MATERIAL

# Sets how many blocks below the player should be checked.
distance: #
```

## Useful links
- [Materials](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)

## Examples

### Checks if the block directly underneath the player is air
```yaml
requirements:
 - type: block below
   block: AIR
```

### Checks if the block 10 blocks below the player is air
```yaml
requirements:
 - type: block below
   block: AIR
   distance: 10
```

### Checks if the player is standing above stone or grass
```yaml
requirements:
 - type: block below
   blocks:
    - STONE
    - GRASS_BLOCK
```

### Checks if the block 5 blocks below the player is water or lava
```yaml
requirements:
 - type: block below
   blocks:
    - WATER
    - LAVA
   distance: 5
```
