# trigger

**Action tag**  
`@trigger`, `@trigger-id`

**Description**
<br>Allows one action to trigger another.  
- `@trigger=id` is the **triggerer** — it calls another action.  
- `@trigger-id=id` is the **receiver** — it runs when triggered by `@trigger`.  

You can connect actions this way to build sequences or chain follow-up actions.

## Syntax

### Single trigger
```yaml
actions:
 - "[message] Hello World!@trigger=test"
 - "[message] Triggered by test!@trigger-id=test"
```

### Multiple triggers
```yaml
actions:
 - "[message] Hello World!@trigger={test1,test2}"
 - "[message] Triggered by test1 or test2!@trigger-id={test1,test2}"
```
> You can assign multiple trigger IDs by wrapping them in { } and separating with commas.  
> In this example, the second action will run if either test1 or test2 is triggered.

## Examples

### Trigger a follow-up message
```yaml
actions:
 - "[message] &aStart action...@trigger=start"
 - "[message] &bThis runs because start was triggered!@trigger-id=start"
```

### Randomly warp players to one of multiple paths
```yaml
actions:
 - "[message] &aPath A chosen!@group=paths@trigger=path-a"
 - "[message] &bPath B chosen!@group=paths@trigger=path-b"

 # Follow-up actions
 - "[console] warp path-a {player}@trigger-id=path-a"
 - "[console] warp path-b {player}@trigger-id=path-b"
```



