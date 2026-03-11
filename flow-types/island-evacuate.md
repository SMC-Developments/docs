# island-evacuate

**Flow type**
<br>`island-evacuate`

**Description**
<br>The island-evacuate flow type teleports all players currently on the player's island to a specified location.

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

Sets the location where players on the island will be teleported to.

### routes
```yaml
routes: LIST
```
> *Example:*
> ```yaml
> routes:
>  - to: FLOW_ID
>    result: pass
>  - to: FLOW_ID
>    result: fail
> ```

> *Route options:*
> - `result` — Specifies which condition result (`pass` or `fail`) this route applies to.

Sets the transition that occurs after the evacuation is executed.
