# number

**Result type**
<br>`number`

**Description**
<br>The number result type returns a formatted numeric value based on a calculation result.

## Syntax
```yaml
- id: RESULT_ID
  type: number
  calculation: CALCULATION_ID
  decimals: NUMBER
  suffix: TEXT
```

### calculation
```yaml
calculation: CALCULATION_ID
```
Sets the calculation whose result will be formatted and returned.

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
