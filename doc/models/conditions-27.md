
# Conditions 27

*This model accepts additional fields of type object.*

## Structure

`Conditions27`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Method` | [`Method?`](../../doc/models/method.md) | Optional | - |
| `Values` | [`Values99?`](../../doc/models/values-99.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "xor",
  "values": "previous_transaction_id",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

