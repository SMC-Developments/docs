# action

**Flow type**
<br>`action`

**Description**
<br>The action flow type executes one or more configured actions.
<br>Actions can be used to send messages, play sounds, open menus, or run other supported operations.
<br>This node does not produce a `pass` or `fail` result by default and will continue by routing to the next node.

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
(Optional) Sets a per-player cooldown (in seconds) for executing this node.
<br>If omitted, the node can execute without cooldown.

### actions
```yaml
actions: LIST
```
Sets the actions that are executed by this node.

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
