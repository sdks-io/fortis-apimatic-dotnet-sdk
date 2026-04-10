
# Joi 4

*This model accepts additional fields of type object.*

## Structure

`Joi4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Conditions` | [`Joi4Conditions`](../../doc/models/containers/joi-4-conditions.md) | Optional | This is a container for any-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "conditions": {
    "method": "oxor",
    "values": "token_api_id",
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

