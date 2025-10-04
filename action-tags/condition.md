# condition

**Action tag**  
`@condition`

**Description**
<br>Adds one or more requirements that must be met before the action can run.

> To add multiple conditions, separate them with `;`.  
> All conditions must be true for the action to run.

## Syntax

### permission
```
[message] Hello World!@condition={type:permission,permission:has.permission}
```
#### Arguments
- **type** — Must be set to `permission`.
- **permission** — The permission the player must have.

### comparator
```
[message] Hello World!@condition={type:>=,input:%placeholder%,output:<value>}
```
#### Arguments
- **type** — The comparison operator (`==`, `!=`, `>=`, `<=`, etc.).
- **input** — The placeholder or value to check.  
- **output** — The expected value to compare against.

#### Comparators list
| Comparator | Description                              |
| ---------- | ---------------------------------------- |
| `==`       | `input` equals `output`                      |
| `!=`       | `input` does not equal `output`              |
| `>`        | `input` is greater than `output`             |
| `<`        | `input` is less than `output`                |
| `>=`       | `input` is greater than or equal to `output` |
| `<=`       | `input` is less than or equal to `output`    |

## Examples

### Send a message only if the player has a permission
```yaml
actions:
 - "[message] &aYou have VIP access!@condition={type:permission,permission:rank.vip}"
```

### Give a diamond only if multiple conditions are true
```yaml
actions:
 - "[giveitem] DIAMOND;1@condition={type:permission,permission:rank.vip;type:>=,input:%smclevels_current_player-levels%,output:10}"
```








