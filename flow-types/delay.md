# delay

**Flow type**
<br>`delay`

**Description**
<br>The delay flow type pauses the flow for a configured duration before continuing.
<br>This can be used for staged onboarding sequences, timed messages, or cinematic effects.
<br>After the delay completes, the flow continues by routing to the next node.

## Syntax
```yaml
- id: FLOW_ID
  type: delay
  duration: NUMBER
  routes: LIST
```

### duration
```yaml
duration: NUMBER
```
Sets how long the flow should wait before continuing.

> *Example:*
> ```yaml
> duration: 3 ## seconds
> ```

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

## Examples

### example-1
```yaml
- id: delay-example
  type: delay
  duration: 3 ## seconds
  routes:
   - to: next-step
```
