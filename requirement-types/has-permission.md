# has permission

**Requirement type**
<br>`has permission`

**Description**
<br>Checks if the player has the specified permission.

## Syntax
```yaml
type: has permission

# Sets the permission node the player must have.
permission: "TEXT"
```

## Examples

### Checks if the player has the rank.owner permission
```yaml
requirements:
 - type: has permission
   permission: rank.owner
```
