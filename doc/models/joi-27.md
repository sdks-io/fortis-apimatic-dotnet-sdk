
# Joi 27

*This model accepts additional fields of type object.*

## Structure

`Joi27`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Conditions` | [`Conditions27`](../../doc/models/conditions-27.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "conditions": {
    "method": "xor",
    "values": "previous_transaction_id",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

