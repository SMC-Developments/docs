# range

**Source type**
<br>`range`

**Description**
<br>The range source type returns a value based on a matching numeric range.

## Syntax
```yaml
- id: SOURCE_ID
  type: range
  default: VALUE
  ranges: LIST
```

### default
```yaml
default: VALUE
```
Sets the value returned when no configured range matches the evaluated value.
<br>If omitted, the source returns `0`.

### ranges
```yaml
ranges: LIST
```
> *Example range:*
> ```yaml
> ranges:
>  - from: NUMBER
>    to: NUMBER
>    value: VALUE
> ```
Sets the configured ranges used to determine the returned value.

### value
```yaml
value: VALUE
```
> *Supports:*
> - [`PlaceholderAPI`](https://wiki.placeholderapi.com/) — Allows metrics to retrieve values from any installed PlaceholderAPI expansion.
> - `variables` — Allows metrics to retrieve values from SMC-Core variable placeholders.

Sets the value returned when the evaluated value falls within this range.
