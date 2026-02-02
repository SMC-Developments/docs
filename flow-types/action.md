# action

**Flow type**
<br>`action`

**Description**
<br>The action flow type executes one or more configured actions.

## Syntax
```yaml
- id: FLOW_ID
  type: action
  target: TARGET
  cooldown: INTEGER
  actions: LIST
  routes: LIST
```

### target
```yaml
target: TARGET
```
> *Supports:*
> - `self` — Executes actions only for the player triggering the flow.
> - `island` — Executes actions for all players currently on the player's island.

Sets which players the actions are executed for.
<br>If omitted, the target defaults to `self`.

### cooldown
```yaml
cooldown: INTEGER
```
Sets a per-player cooldown (in seconds) after executing this node. 
<br>If the same node is reached again for the same player while the cooldown is active, the node will not execute.
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
