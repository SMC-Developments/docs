# launch

**Action type**
<br>`[launch]`

**Description**
<br>Launches the player by applying a velocity. Supports three modes:
- **facing** — jump‑pad style relative to where the player is looking.
- **velocity** — raw x, y, z velocity in world axes (ignores facing).
- **fixed** — launches toward a yaw/pitch with a single power value.

## Syntax

### facing
```
[launch] facing <length> <height> [yaw-offset] [pitch-offset];[options]
```
#### Arguments
- **length** — Sets the horizontal push (in blocks‑feel).
- **height** — Sets the vertical boost (in blocks‑feel).
- **yaw-offset** *(optional)* — Sets extra left/right rotation in degrees (positive = right, negative = left). Default `0`.
- **pitch-offset** *(optional)* — Sets extra up/down tilt in degrees (negative = up, positive = down). Default `0`.

### velocity
```
[launch] velocity <x> <y> <z>;[options]
```
#### Arguments
- **x** — Sets east (+) / west (–) velocity component.
- **y** — Sets up (+) / down (–) velocity component.
- **z** — Sets south (+) / north (–) velocity component.

### fixed
```
[launch] fixed <yaw> <pitch> <power>;[options]
```
#### Arguments
- **yaw** — Sets horizontal angle in degrees (**0 = south**, **90 = west**, **180 = north**, **270 = east**).
- **pitch** — Sets vertical tilt in degrees (**–90 = straight up**, **+90 = straight down**).
- **power** — Sets overall launch strength (scalar).

## Options

Append after the arguments with a semicolon: `;key=value`

- `no-fall=<ticks>` — Sets temporary fall‑damage immunity (in ticks).

## Examples

### Basic jump pad (straight up ~3 blocks)
```yaml
actions:
 - "[launch] facing 0 3;no-fall=60"
```

### Long forward boost with a small hop
```yaml
actions:
 - "[launch] facing 6 1"
```

### Side bumper (90° to the right of facing)
```yaml
actions:
 - "[launch] facing 4 0.4 90;no-fall=40"
```

### Raw vector burst (absolute): up + north
```yaml
actions:
 - "[launch] velocity 0 1.2 -1.1;no-fall=80"
```

### Fixed cannon: always shoot east, slightly upward
```yaml
actions:
 - "[launch] fixed 270 -15 3;no-fall=100"
```

### Cliff portal pad — go **up ~5 blocks**, then **forward** through the portal
```yaml
actions:
 - "[sound] BLOCK_NOTE_BLOCK_PLING 1 1.5"
 - "[particle] CLOUD 12 0.3 0.1 0.3 0.02 false"
 # Step 1: go straight up (~5 blocks) and ignore fall damage briefly
 - "[launch] facing 0 5;no-fall=100"
 # Step 2: after reaching the peak, add a forward shove
 - "[delay] 20"
 - "[launch] facing 6 0.3;no-fall=60"
```

### Cliff portal pad (fixed aim) — ignore player facing, always shoot toward portal
```yaml
actions:
 - "[sound] BLOCK_NOTE_BLOCK_PLING 1 1.5"
 - "[launch] facing 0 5;no-fall=100"
 - "[delay] 20"
 - "[launch] fixed 270 0 2.8;no-fall=80"
```
