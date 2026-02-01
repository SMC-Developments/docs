# island-teleport

**Flow type**
<br>`island-teleport`

**Description**
<br>The island-teleport flow type teleports the player to their island.

## Syntax
```yaml
- id: FLOW_ID
  type: island-teleport
  routes: LIST
```

### routes
```yaml
routes: LIST
```
> *Example:*
> ```yaml
> routes:
>  - to: FLOW_ID
> ```

Sets the transitions that occur after the teleport attempt.