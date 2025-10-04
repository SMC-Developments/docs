# comparator

**Requirement type**
<br>`comparator`

**Description**
<br>Compares an input value with an output value using a comparator (e.g. `==`, `>=`, `<`, etc.).

### Syntax
```yaml
type: "COMPARATOR"

# Sets the input value to compare, often a placeholder.
input: "TEXT"

# Sets the value the input will be compared against.
output: "TEXT"
```

### Comparators list
| Comparator | Description                              |
| ---------- | ---------------------------------------- |
| `==`       | `input` equals `output`                      |
| `!=`       | `input` does not equal `output`              |
| `>`        | `input` is greater than `output`             |
| `<`        | `input` is less than `output`                |
| `>=`       | `input` is greater than or equal to `output` |
| `<=`       | `input` is less than or equal to `output`    |


## Examples

### Checks if the player is OP
```yaml
requirements:
 - type: "=="
   input: "%player_is_op%"
   output: "yes"
```

### Checks if the player's level is at least 10
```yaml
requirements:
 - type: ">="
   input: "%smclevels_current_player-levels%"
   output: "10"
```

### Checks if the player's health is less than 5
```yaml
requirements:
 - type: "<"
   input: "%player_health%"
   output: "5"
```
