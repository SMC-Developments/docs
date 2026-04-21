# confirm

**Flow type**
<br>`confirm`

**Description**
<br>The confirm flow type requests confirmation from the player before continuing the flow.

## Syntax
```yaml
- id: FLOW_ID
  type: confirm
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
>  - to: FLOW_ID
>    result: ignore
> ```

> *Route options:*
> * `result` — Specifies which route result this path applies to. Supported values: `pass`, `fail`, or `ignore`.

Sets the transitions that occur after the player responds to the confirmation.

