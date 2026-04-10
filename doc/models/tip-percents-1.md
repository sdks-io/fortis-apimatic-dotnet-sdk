
# Tip Percents 1

*This model accepts additional fields of type object.*

## Structure

`TipPercents1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Percent1` | `int?` | Optional | field can only contain a value from 0 to 99, if 1 field is NULL, all fields must be null.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `Percent2` | `int?` | Optional | field can only contain a value from 0 to 99, if 1 field is NULL, all fields must be null.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `Percent3` | `int?` | Optional | field can only contain a value from 0 to 99, if 1 field is NULL, all fields must be null.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "percent_1": 0,
  "percent_2": 2,
  "percent_3": 99,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

