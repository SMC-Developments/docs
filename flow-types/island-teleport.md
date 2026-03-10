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
>    result: pass
>    once: true
>  - to: FLOW_ID
>    result: fail
> ```

> *Route options:*
> - `result` — Specifies which condition result (`pass` or `fail`) this route applies to.

Sets the transitions that occur after the teleport attempt.
