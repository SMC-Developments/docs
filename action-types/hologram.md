# hologram

**Action type**
<br>`[hologram]`

**Description**
<br>Displays a temporary hologram in front of the player. Supports three modes:
- **rise** — Hologram rises upward.
- **sticky** — Hologram sticks to the player and follows them.
- **fixed** — Hologram stays fixed at the summoned location.

## Syntax

```
[hologram] <mode> <duration> <y> <text>
```
#### Arguments
- **mode** — Sets how the hologram behaves.
- **duration** — How long the hologram should stay visible (in ticks).
- **y** — Vertical offset in front of the player (e.g. `1.5` to appear just above the head).
- **text** — The text shown in the hologram. Supports color codes, placeholders, and `\n` for new lines.

## Examples

### Rising hologram
```yaml
actions:
 - "[hologram] rise 40 1.5 &a+10 Coins!"
```

### Sticky hologram
```yaml
actions:
 - "[hologram] sticky 60 2 &bQuest Complete!"
```

### Fixed hologram
```yaml
actions:
 - "[hologram] fixed 100 2 &6Treasure Found!"
```

### Multi-line hologram with `\n`
```yaml
actions:
 - "[hologram] rise 80 2 &eTreasure Chest Found!\n&7+100 XP\n&a+5 Coins"
```
