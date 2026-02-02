# island-evacuate

**Flow type**
<br>`island-evacuate`

**Description**
<br>The island-evacuate flow type teleports all players currently on the player's island to a safe location.
<br>This is typically used before deleting or resetting an island to ensure no players remain inside the island region.

## Syntax
```yaml
- id: FLOW_ID
  type: island-evacuate
  location: LOCATION
  routes: LIST
```

### location
```yaml
location: LOCATION
```
Sets the location where players on the island will be teleported to.

> *Example:*
> ```yaml
> location:
>   world: world_spawn
>   x: -44
>   y: 106
>   z: 31
>   yaw: -40.5
>   pitch: -3.0
> ```

### routes
```yaml
routes: LIST
```
> *Example:*
> ```yaml
> routes:
>  - to: FLOW_ID
> ```

Sets the transition that occurs after the evacuation is executed.

## Behavior

- This node does not produce a `pass` or `fail` result.
- After evacuation, the flow continues using the configured route.

## Examples

### example-1
```yaml
- id: evacuate-island
  type: island-evacuate
  location:
    world: world_spawn
    x: -44
    y: 106
    z: 31
    yaw: -40.5
    pitch: -3.0
  routes:
   - to: execute-island-deletion
```
