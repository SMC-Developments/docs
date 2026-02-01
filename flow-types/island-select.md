# island-select

**Flow type**
<br>`island-select`

**Description**
<br>The island-select flow type lets a player choose which island schematic to use for island creation.

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
> *Example:*
> ```yaml
> schematics:
>  - "default"
>  - "desert"
>  - "forest"
> ```

Sets which schematic ids can be selected.
<br>If omitted, all available schematics are allowed.

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
