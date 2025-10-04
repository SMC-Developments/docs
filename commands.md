# Commands
Commands allow you to bind actions to custom commands.
<br>They can be registered for players only, or universally for both players and the console.

### Syntax
```yaml
# universal-commands:
player-commands:
  register: BOOLEAN
  trigger-actions: ACTIONS
  commands: COMMANDS
```
> *Note: You may see `player-commands` and `universal-commands`.  
> player-commands are strictly for player use and will not work when used by the console, whereas universal-commands will work for both players and the console.*

### register
```yaml
register: BOOLEAN
```
If set to true, the command will be registered, making it appear in the command tab list.

### trigger actions
```yaml
trigger-actions: ACTIONS
```
Sets the actions to run when the command is executed.
<br>Actions execute from top to bottom in the list.
<br>Check the [Actions](actions.md) section for more information.

### commands
```yaml
commands: COMMAND
```
> *Multiple commands:*  
> ```yaml
> commands:
>  - COMMAND_1
>  - COMMAND_2
> ```
Sets the command that triggers the specified feature.



