# island-select

**Flow type**
<br>`island-select`

**Description**
<br>The island-select flow type lets a player choose which island schematic to use for island creation.
<br>This node typically opens a selection GUI and stores the chosen schematic for later steps (for example, for `island-create`).
<br>If the player completes a selection, the result is `pass`. If the selection is cancelled or times out, the result is `fail`.

## Syntax
```yaml
- id: FLOW_ID
  type: island-select
  schematics: LIST
  routes: LIST
```

### schematics
```yaml
schematics: LIST
```
(Optional) Sets which schematic ids can be selected.
<br>If omitted, all available schematics are allowed.

> *Example:*
> ```yaml
> schematics:
>  - "default"
>  - "desert"
>  - "forest"
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
Sets the transitions that occur after selection is completed.

## Examples

### example-1
```yaml
- id: island-select-example
  type: island-select
  schematics:
   - "default"
   - "example"
  routes:
   - to: island-create
     result: pass
   - to: end
     result: fail
```
