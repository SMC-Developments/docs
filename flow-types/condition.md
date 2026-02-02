# condition

**Flow type**
<br>`condition`

**Description**
<br>The condition flow type checks whether the player meets the configured conditions.
<br>If the conditions pass, the node produces a pass result. If they do not pass, the node produces a fail result.

## Syntax
```yaml
- id: FLOW_ID
  type: condition
  active: BOOLEAN
  conditions: CONDITIONS
  routes: LIST
```

### active
```yaml
active: BOOLEAN
```
If set to true, this condition is always checked.
<br>If set to false (default), this condition is only checked when routed.

### conditions
```yaml
conditions: CONDITIONS
```
Sets the conditions that are evaluated by this node.
<br>Check the [Conditions](https://github.com/VinceSMC/SMC-Developments/blob/main/documentation/conditions.md) section for more information.

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
> - `once` — If set to true, this route can only be taken once per player.

Sets the transitions that occur after the condition is evaluated.
