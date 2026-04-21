# delay

**Flow type**
<br>`delay`

**Description**
<br>The delay flow type pauses the flow for a configured duration before continuing.

## Syntax
```yaml
- id: FLOW_ID
  type: delay
  duration: INTEGER
  routes: LIST
```

### duration
```yaml
duration: INTEGER
```
Sets how long the flow should wait before continuing in ticks.

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

Sets the transitions that occur after the delay completes.
