# action

**Flow type**
<br>`action`

**Description**
<br>The action flow type executes one or more configured actions.

## Syntax
```yaml
- id: FLOW_ID
  type: action
  cooldown: NUMBER
  actions: LIST
  routes: LIST
```

### cooldown
```yaml
cooldown: NUMBER
```
Sets a per-player cooldown (in seconds) for executing this node.
<br>If omitted, the node can execute without cooldown.

### actions
```yaml
actions: LIST
```
Sets the actions that are executed by this node.
<br>Check the [Actions](https://github.com/VinceSMC/SMC-Developments/blob/f5a97c218bf83512aa6d5232cb35e18444c6d88d/documentation/actions.md) section for more information.

### routes
```yaml
routes: LIST
```
> *Example:*
> ```yaml
> routes:
>  - to: FLOW_ID
> ```
Sets the transitions that occur after actions are executed.

## Examples

### example-1
```yaml
- id: island-created
  type: action
  actions:
   - "[message] &aYour island has been created!"
  routes:
   - to: end
```
