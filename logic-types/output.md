# output

**Type**
<br>`output`

**Description**
<br>The output response type checks whether the evaluated value matches the configured output value.
<br>If the values match, the configured return value will be used.

## Syntax
```yaml
- output: TEXT
  return: TEXT
```

### output
```yaml
output: TEXT
```
> *Example:*
> ```yaml
> output: "Yes"
> ```
> Checks whether the evaluated input value matches the configured output value.
> <br>If true, the return value of this response will be used.

Sets the value that must match the evaluated input value.

### return
```yaml
return: TEXT
```

Sets the value returned when the output matches.

