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

### conditions
```yaml
conditions: CONDITIONS
```
Sets conditions that must pass to allow the command to continue.
<br>If omitted, this node is treated as a pass result when the command matches.
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

Sets the transitions that occur after the command is processed.
