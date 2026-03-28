# variable

**Action type**
<br>`[variable]`

**Description**
<br>Resolves a variable and sends the resulting text to the player. Supports dynamic parameter replacement using key=value pairs, which are injected into placeholders (e.g. `{placeholder}`) defined in the variable.

## Syntax
```
[variable] <fileID> <variableID>;[parameters]
```

#### Arguments
- **fileID** — Sets the variable file identifier.
- **variableID** — Sets the variable identifier inside the file.

## Parameters

Append after the arguments with a semicolon: `;key=value`

- `key=value` — Sets a parameter used to replace a matching placeholder in the variable (e.g. `{requirement}`).

## Examples

### Basic usage
```yaml
actions:
 - "[variable] messages consume-requirement;requirement=Potato Collection VI"
```

### With placeholders
```yaml
actions:
 - "[variable] messages consume-requirement;requirement=%smccollections_display-name_potato% Collection VI"
```