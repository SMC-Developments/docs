# playback

**Effect component**
<br>`playback`

**Description**
<br>The playback component controls how an effect timeline is played and rendered.

> [!NOTE]
> Effect playback is global. Every use of the same effect placeholder shares one timeline position, regardless of the player or location displaying it.

## Syntax
```yaml
playback:
  mode: TEXT
  frame-rate: NUMBER
```

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
