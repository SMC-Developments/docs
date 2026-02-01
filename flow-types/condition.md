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
>  - to: FLOW_ID
>    result: fail
> ```
Sets the transitions that occur after the condition is evaluated.

## Examples

### example-1
```yaml
- id: check
  type: condition
  conditions:
    requirements:
     - type: "=="
       input: "{player-has-island}"
       output: "false"
  routes:
   - to: force-create
     result: pass
   - to: has-island
     result: fail
```
