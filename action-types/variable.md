# variable

**Action type**
<br>`[variable]`

**Description**
<br>Resolves a variable and sends the resulting text to the player.

## Syntax
```
[variable] <fileID> <variableID>;[parameters]
```

#### Arguments
- **fileID** — Sets the variable file identifier.
- **variableID** — Sets the variable identifier inside the file.

## Parameters

Append after the arguments with a semicolon: `;param=value`
- `param=value` — Sets a parameter used to replace a matching placeholder in the variable (e.g. `{example}`).

## Examples

### Basic usage
```yaml
actions:
 - "[variable] text cooldown;time=30 seconds"
```

### With PAPI placeholders
```yaml
actions:
 - "[variable] text requirement;requirement=%smccollections_display-name_potato% Collection VI"
```
