# number

**Result type**
<br>`number`

**Description**
<br>The number result type returns a formatted numeric value based on an input value.

## Syntax
```yaml
- id: RESULT_ID
  type: number
  input: VALUE
  decimals: NUMBER
  suffix: TEXT
```

### input
```yaml
input: VALUE
```
> *Supports:*
> - `{src_SOURCE_ID}` — Allows results to reference values returned by configured sources.
> - `{calc_CALCULATION_ID}` — Allows results to reference values returned by calculations.

Sets the value that will be formatted and returned.

### decimals
```yaml
decimals: NUMBER
```
Sets the amount of decimal places the number will be formatted with.
<br>If omitted, the number is returned without decimal formatting.

### suffix
```yaml
suffix: TEXT
```
Sets the text appended to the formatted number.
<br>This is commonly used for units or percentages.

