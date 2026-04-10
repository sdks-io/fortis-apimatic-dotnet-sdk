
# Response Token

*This model accepts additional fields of type object.*

## Structure

`ResponseToken`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type92?`](../../doc/models/type-92.md) | Optional | - |
| `Data` | [`Data25`](../../doc/models/data-25.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Token",
  "data": {
    "account_holder_name": "account_holder_name0",
    "account_vault_api_id": "account_vault_api_id4",
    "token_api_id": "token_api_id6",
    "accountvault_c1": "accountvault_c14",
    "accountvault_c2": "accountvault_c28",
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

