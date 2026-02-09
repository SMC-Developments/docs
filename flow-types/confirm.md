# confirm

**Flow type**  
<br>`confirm`

**Description**  
<br>The confirm flow type requests confirmation from the player before continuing the flow.  
<br>If the player confirms the action, the node produces a **pass** result.  
<br>If the player cancels the action, the node produces a **fail** result.

This flow type is used for actions that require player confirmation before execution.

---

## Syntax
```yaml
- id: FLOW_ID
  type: confirm
  routes: LIST
```

---

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

> *Route options:*
> - `result` — Specifies which confirm result (`pass` or `fail`) this route applies to.
> - `once` — If set to true, this route can only be taken once per player.

Sets the transitions that occur after the player responds to the confirmation.