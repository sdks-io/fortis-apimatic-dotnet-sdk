
# Joi

*This model accepts additional fields of type object.*

## Structure

`Joi`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Conditions` | [`Conditions`](../../doc/models/conditions.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "conditions": {
    "method": "xor",
    "values": "account_vault_api_id",
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

