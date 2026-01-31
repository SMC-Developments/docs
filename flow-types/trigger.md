# trigger

**Flow type**
<br>`trigger`

**Description**
<br>The trigger flow type defines an entry point for a flow that reacts to a specific event, such as a player joining the server.
<br>When a trigger is active, it listens for its configured event and, when fired, begins flow execution by routing to the next defined node.
<br>Triggers do not perform logic themselves, they only start or resume a flow.

## Syntax
```yaml
- id: FLOW_ID
  type: trigger
  trigger: TRIGGER_ID
  active: BOOLEAN
  routes: LIST
```

### trigger
```yaml
trigger: TRIGGER_ID
```
> *Supports:*
> - `on-join` — Fired when a player joins the server.

Sets the event that activates this trigger.

### active
```yaml
active: BOOLEAN
```
If set to true, this trigger is always listening for its configured event.
<br>If set to false (default), the trigger will only be executed when reached via a flow route.

### routes
```yaml
routes: LIST
```

## Examples

### example-1
```yaml
example-here
```














