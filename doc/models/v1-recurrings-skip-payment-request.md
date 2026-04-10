
# V1 Recurrings Skip Payment Request

*This model accepts additional fields of type object.*

## Structure

`V1RecurringsSkipPaymentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SkipCount` | `int` | Required | Skip Count<br><br>**Constraints**: `>= 1`, `<= 99` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "skip_count": 7,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

