# condition

**Flow type**
<br>`condition`

**Description**
<br>The condition flow type evaluates a configured conditions block and produces a boolean result.
<br>If the configured requirements pass, the result is `pass`. If they do not pass, the result is `fail`.
<br>The next node is chosen by routing based on the result.

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
If set to true, this node is always evaluated when its parent trigger is fired.
<br>If set to false (default), the node will only be executed when reached via a flow route.

### conditions
```yaml
conditions: CONDITIONS
```
Sets the conditions that are evaluated by this node.

> This uses the same conditions format used throughout the plugin.
> When requirements pass, the node result becomes `pass`. Otherwise, the result becomes `fail`.

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
