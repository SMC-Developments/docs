# teleport

**Action type**
<br>`[teleport]`

**Description**
<br>Teleports the player to a specific location in a given world.

## Syntax
```
[teleport] <world> <x> <y> <z> <yaw> <pitch>
```
#### Arguments
- **world** — The world name.
- **x** — X coordinate.
- **y** — Y coordinate.
- **z** — Z coordinate.
- **yaw** — The player’s facing direction (in degrees).
- **pitch** — The player’s vertical angle (in degrees).

## Examples

### Teleport player to spawn
```yaml
actions:
 - "[teleport] world_spawn 0 64 0 0 0"
```
