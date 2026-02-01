# command

**Flow type**
<br>`command`

**Description**
<br>The command flow type listens for a command pattern and starts or continues the flow when the command is executed.

## Syntax
```yaml
- id: FLOW_ID
  type: command
  command: TEXT
  active: BOOLEAN
  conditions: CONDITIONS
  routes: LIST
```

### command
```yaml
command: TEXT
```
> *Multiple commands:*
> ```yaml
> commands:
>  - COMMAND_1
>  - COMMAND_2
>  - COMMAND_3
> ```
Sets the command pattern that activates this node.

### active
```yaml
active: BOOLEAN
```
If set to true, this command listener is always active.
<br>If set to false (default), the node will only be executed when reached via a flow route.

### conditions
```yaml
conditions: CONDITIONS
```
(Optional) Sets conditions that must pass to allow the command to continue.

> If conditions are omitted, this node is treated as a `pass` result when the command matches.

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
Sets the transitions that occur after the command is processed.

## Examples

### example-1
```yaml
- id: island-create-command
  type: command
  command: "is create"
  active: true
  routes:
   - to: check
     result: pass
```
