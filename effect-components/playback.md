# playback

**Effect component**
<br>`playback`

**Description**
<br>The playback component controls how an effect timeline is played and rendered.

## Syntax
```yaml
playback:
  mode: TEXT
  frame-rate: NUMBER
```

> [!NOTE]
> Effect playback is global. Every use of the same effect placeholder shares one timeline position, regardless of the player or location displaying it.
> <br>Playback begins when the effect is loaded or reloaded.
>
> PlaceholderAPI does not indicate whether resolved output is currently visible. Effects therefore do not start or restart when a menu, boss bar, entity display, or other destination becomes visible.

### mode
```yaml
mode: TEXT
```
> *Supported values:* `loop`, `ping-pong`, `static`  
> *Default value:* `loop`

Sets how the effect timeline is played.

| Mode | Description |
|---|---|
| `loop` | Repeats the timeline continuously. |
| `ping-pong` | Plays the timeline forward and then in reverse. |
| `static` | Renders one fixed state using only the root style and root layers. A timeline is not required. |

### frame rate
```yaml
frame-rate: NUMBER
```
> *Supported values:* `1` to `20`  
> *Default value:* `20`

Sets the maximum number of rendered states generated per second.
<br>The frame rate controls the smoothness of an effect, but does not change how long its timeline stages last.

| Frame rate | Time per rendered state |
|---|---|
| `5` | `200ms` |
| `10` | `100ms` |
| `20` | `50ms` |

> [!NOTE]
> The visible frame rate can be limited by how often the location displaying the placeholder is updated.

## Examples

### Loop an effect at 20 frames per second
```yaml
playback:
  mode: loop
  frame-rate: 20
```

### Play an effect once after it is loaded or reloaded
```yaml
playback:
  mode: once
  frame-rate: 10
```
