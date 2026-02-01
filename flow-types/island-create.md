# island-create

**Flow type**
<br>`island-create`

**Description**
<br>The island-create flow type creates an island using the configured schematic.
<br>If island creation succeeds, the result is `pass`. If it fails, the result is `fail`.
<br>This node should be used after selection/validation steps such as `condition` and `island-select`.

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

> *Example:*
> ```yaml
> schematic: default
> ```

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
Sets the transitions that occur after island creation completes.

## Examples

### example-1
```yaml
- id: force-create
  type: island-create
  schematic: default
  routes:
   - to: island-created
     result: pass
   - to: creation-failed
     result: fail
```
