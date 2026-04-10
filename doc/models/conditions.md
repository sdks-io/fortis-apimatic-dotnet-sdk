
# Conditions

*This model accepts additional fields of type object.*

## Structure

`Conditions`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Method` | [`Method?`](../../doc/models/method.md) | Optional | - |
| `Values` | [`Values?`](../../doc/models/values.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "xor",
  "values": "account_vault_id",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

