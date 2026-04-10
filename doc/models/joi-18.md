
# Joi 18

*This model accepts additional fields of type object.*

## Structure

`Joi18`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Conditions` | [`Joi18Conditions`](../../doc/models/containers/joi-18-conditions.md) | Optional | This is a container for any-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "conditions": {
    "method": "xor",
    "values": "account_number",
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

