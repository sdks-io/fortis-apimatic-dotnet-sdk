
# V1 Recurrings Defer Payment Request

*This model accepts additional fields of type object.*

## Structure

`V1RecurringsDeferPaymentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeferCount` | `int` | Required | Defer Count<br><br>**Constraints**: `>= 1`, `<= 99` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "defer_count": 5,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

