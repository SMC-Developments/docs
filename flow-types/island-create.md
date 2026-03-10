# island-create

**Flow type**
<br>`island-create`

**Description**
<br>The island-create flow type creates an island using the configured schematic.

## Syntax
```yaml
- id: FLOW_ID
  type: island-create
  schematic: TEXT
  routes: LIST
```

### schematic
```yaml
schematic: TEXT
```
Sets the schematic id to use for island creation.

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

Sets the transitions that occur after island creation completes.
