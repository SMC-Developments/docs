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
>  - to: FLOW_ID
>    result: fail
>  - to: FLOW_ID
>    result: ignore
> ```

> *Route options:*
> * `result` — Specifies which route result this path applies to. Supported values: `pass`, `fail`, or `ignore`.

Sets the transitions that occur after the teleport attempt.
