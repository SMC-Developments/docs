# sound

**Action type**
<br>`[sound]`

**Description**
<br>Plays a sound effect for the player.

## Syntax
```
[sound] <sound> <volume> <pitch>
```
#### Arguments
- **sound** — The sound name (see Sound Types link below).
- **volume** — The sound’s volume. Default is `1`.
- **pitch** — The sound’s pitch. Default is `1`.

## Useful links
- [Sound Types](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Sound.html)

## Examples

### Play a level-up sound
```yaml
actions:
 - "[sound] ENTITY_PLAYER_LEVELUP 1 1"
```

### Play a pickup sound with higher pitch
```yaml
actions:
 - "[sound] ENTITY_ITEM_PICKUP 1 2"
```
