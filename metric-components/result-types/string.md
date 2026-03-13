# string

**Result type**
<br>`string`

**Description**
<br>The string result type returns formatted text based on a calculation result.

## Syntax
```yaml
- id: RESULT_ID
  type: string
  format: TEXT
```

### format
```yaml
format: TEXT
```
> *Supports:*
> - `{SOURCE_ID}` — Allows results to reference values returned by configured sources.
> - `{CALCULATION_ID}` — Allows results to reference values returned by calculations.
> - `{RESULT_ID}` — Allows results to reference other formatted results.

Sets the formatted text returned by the result.


