# placeholder

**Source type**
<br>`placeholder`

**Description**
<br>The placeholder source type returns the value of a placeholder.

## Syntax
```yaml
- id: SOURCE_ID
  type: placeholder
  placeholder: PLACEHOLDER
```

### placeholder
```yaml
placeholder: PLACEHOLDER
```
> *Supports:*
> - [`PlaceholderAPI`](https://wiki.placeholderapi.com/) — Allows metrics to retrieve values from any installed PlaceholderAPI expansion.
> - `variables` — Allows metrics to retrieve values from SMC-Core variable placeholders.

Sets the placeholder used to retrieve the source value.


