# cooldown

**Action tag**  
`@cooldown`

**Description**
<br>Adds a cooldown to the action. This limits how often it can be triggered within a set time.
> The default cooldown duration is set in the core configuration file.

## Examples

### Prevent players from spamming a message
```yaml
actions:
 - "[message] You can't spam me!@cooldown"
```


