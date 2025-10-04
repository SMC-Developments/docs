# broadcast

**Action tag**  
`@broadcast`

**Description**
<br>Sends the action to all online players.

## Examples

### Sends the text "Hello World!" to all online players
```yaml
actions:
 - "[message] Hello World!@broadcast"
```

### Broadcast a welcome title when a new player joins
```yaml
actions:
 - "[title] &a{player} joined!;&7Everyone say welcome!;10;60;10@broadcast"
```
