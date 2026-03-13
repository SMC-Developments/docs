# formula

**Calculation type**
<br>`formula`

**Description**
<br>The formula calculation type evaluates a mathematical expression and returns the resulting value.

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
> - [`EvalEx`](https://ezylang.github.io/EvalEx/) — Provides mathematical functions and operators used to evaluate expressions.

Sets the mathematical expression that will be evaluated to produce the calculation result.

Values from sources or other calculations can be referenced using placeholders.

> *Example:*
> ```yaml
> formula: "{levels-combat} + {levels-farming}"
> ```

This will return the sum of the referenced values.