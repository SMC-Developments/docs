# Metrics Example

```yaml
# These are the source values, which you can use inside the calculations.
sources:
 - id: current-value
   type: value
   value: "%current-value%"

 - id: maximum-value
   type: value
   value: "%maximum-value%"

# Here you can use the source values to create different calculations.
calculations:
 - id: current
   type: formula
   formula: "{src_current-value}"

 - id: maximum
   type: formula
   formula: "{src_maximum-value}"

 - id: remaining
   type: formula
   formula: "MAX(0, {calc_maximum} - {calc_current})"

 - id: percentage
   type: formula
   formula: "IF({calc_maximum} <= 0, 0, ({calc_current} / {calc_maximum}) * 100)"

# Here you can format the calculations into usable results such as a number, progress-bar, a string etc.
results:
 - id: current # {metric--FileID_current}
   type: number
   input: "{calc_current}"
   decimals: 0

 - id: maximum # {metric--FileID_maximum}
   type: number
   input: "{calc_maximum}"
   decimals: 0

 - id: remaining # {metric--FileID_remaining}
   type: number
   input: "{calc_remaining}"
   decimals: 0

 - id: percentage # {metric--FileID_percentage}
   type: number
   input: "{calc_percentage}"
   decimals: 1
   suffix: "%"

 - id: progress-bar # {metric--FileID_progress-bar}
   type: progress-bar
   current: "{calc_current}"
   maximum: "{calc_maximum}"
   symbol: "|"
   length: 24
   color-filled: "&b"
   color-partial: "&f"
   color-empty: "&7"

 - id: fraction # {metric--FileID_fraction}
   type: string
   format: "{res_current}/{res_maximum}"

 - id: progress-line # {metric--FileID_progress-line}
   type: string
   format: "{res_progress-bar} &b{res_fraction}"
```
