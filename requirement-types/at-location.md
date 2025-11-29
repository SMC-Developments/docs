# at location

**Requirement type**
<br>`at location`

**Description**
<br>Checks if the player is at the specified world and coordinates.

## Syntax
```yaml
type: at location

# Sets the world the player must be in.
world: "WORLD_NAME"

# Sets the required coordinates.
x: #
y: #
z: #
```

## Examples

### Checks if the player is at (0, 0, 0) in world `world_dev`
```yaml
requirements:
 - type: at location
   world: world_dev
   x: 0
   y: 0
   z: 0
```

### Checks if the player is standing at Y-level 100 in the overworld
```yaml
requirements:
 - type: at location
   world: world
   x: 50
   y: 100
   z: -20
```
