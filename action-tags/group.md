# group

**Action tag**  
`@group`

**Description**
<br>Lets you group multiple actions. When the group runs, only one action from it will be chosen at random.

## Examples

### Show players one random message, each time it gets triggered
```yaml
actions:
 - "[message] &aThe portal glows brightly!@group=portal"
 - "[message] &bThe portal hums quietly...@group=portal"
 - "[message] &cThe portal crackles with energy!@group=portal"
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
