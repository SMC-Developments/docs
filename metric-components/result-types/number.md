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
  args: ARGUMENTS
```

### calculation
```yaml
calculation: CALCULATION_ID
```
Sets the calculation whose result will be formatted and returned.

### args
```yaml
args: ARGUMENTS
```
> *Structure:*
> ```yaml
> args:
>   decimals: NUMBER
>   suffix: TEXT
> ```

Sets the optional formatting arguments used when returning the number result.
