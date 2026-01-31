# trigger

**Flow type**
<br>`trigger`

**Description**
The trigge` flow type defines an entry point for a flow that reacts to a specific event, such as a player joining the server.

When a trigger is active, it listens for its configured event and, when fired, begins flow execution by routing to the next defined node.

Triggers do not perform logic themselves, they only start or resume a flow.

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
> - `on-join` — TEXT

Sets the trigger to activate this flow.

### active
```yaml
active: BOOLEAN
```

### routes
```yaml
routes: LIST
```

## Examples

### example-1
```yaml
example-here
```











