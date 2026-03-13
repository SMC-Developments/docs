# condition

**Logic response type**
<br>`condition`

**Description**
<br>The condition response type evaluates the input value using a comparator expression.

## Syntax
```yaml
- condition: EXPRESSION
  return: TEXT
```

### condition
```yaml
condition: EXPRESSION
```
Sets the comparison expression used to evaluate the input value.

### return
```yaml
return: TEXT
```
Sets the value returned when the condition matches.

### Comparators list

| Comparator | Description |
|-----------|-------------|
| `==` | `input` equals `output` |
| `!=` | `input` does not equal `output` |
| `>` | `input` is greater than `output` |
| `<` | `input` is less than `output` |
| `>=` | `input` is greater than or equal to `output` |
| `<=` | `input` is less than or equal to `output` |