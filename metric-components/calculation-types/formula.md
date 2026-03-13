# formula

**Calculation type**
<br>`formula`

**Description**
<br>The formula calculation type evaluates a mathematical expression and returns the resulting value.
<br>Calculations are powered by [EvalEx](https://ezylang.github.io/EvalEx/).

## Syntax
```yaml
- id: CALCULATION_ID
  type: formula
  formula: TEXT
```

### formula
```yaml
formula: TEXT
```
> *Supports:*
> - `sources` — Allows calculations to reference values returned by configured sources.
> - `calculations` — Allows calculations to reference values returned by other calculations.

Sets the mathematical expression that will be evaluated to produce the calculation result.
<br>Values from sources or other calculations can be referenced using placeholders.

