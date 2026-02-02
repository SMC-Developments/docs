# island-delete

**Flow type**
<br>`island-delete`

**Description**
<br>The island-delete flow type deletes the player's current island.
<br>This node is typically used in island reset flows where the island is removed and then replaced with a new one.

## Syntax
```yaml
- id: FLOW_ID
  type: island-delete
  routes: LIST
```

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

Sets the transitions that occur after the delete attempt.

## Behavior

- If the island is deleted successfully, the node result is `pass`.
- If the island could not be deleted, the node result is `fail`.

## Examples

### example-1
```yaml
- id: delete-island
  type: island-delete
  routes:
   - to: provision-new-island
     result: pass
   - to: reset-failed
     result: fail
```
