# island-delete

**Flow type**
<br>`island-delete`

**Description**
<br>The island-delete flow type deletes the player's current island.

## Syntax
```yaml
- id: FLOW_ID
  type: island-delete
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
> ```

> *Route options:*
> - `result` — Specifies which condition result (`pass` or `fail`) this route applies to.

Sets the transitions that occur after the delete attempt.
