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
> ```
Sets the transitions that occur after the delay completes.
