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
>    once: true
>  - to: FLOW_ID
>    result: fail
> ```

> *Route options:*
> - `result` — Specifies which condition result (`pass` or `fail`) this route applies to.

Sets the transitions that occur after selection is completed.
