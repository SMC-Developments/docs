# particle

**Action type**
<br>`[particle]`

**Description**
<br>Displays a particle effect at the player’s location.

## Syntax
```
[particle] <particle> <amount> <offset-x> <offset-y> <offset-z> <speed> <visible-all>
```
#### Arguments
- **particle** — The particle type.
- **amount** — The number of particles to display.
- **offset-x** — Random spread on the X axis.
- **offset-y** — Random spread on the Y axis.
- **offset-z** — Random spread on the Z axis.
- **speed** — The particle’s movement speed.
- **visible-all** — Whether the particle is visible to all players (`true`) or only to the player (`false`).

## Useful links
- [Particles](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Particle.html)

## Examples

### Display 10 hearts around the player
```yaml
actions:
 - "[particle] HEART 10 0.5 1 0.5 0 false"
```

### Flame burst visible to everyone
```yaml
actions:
 - "[particle] FLAME 30 0.2 0.2 0.2 0.05 true"
```
