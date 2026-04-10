
# Response Recurring

*This model accepts additional fields of type object.*

## Structure

`ResponseRecurring`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type67?`](../../doc/models/type-67.md) | Optional | - |
| `Data` | [`Data20`](../../doc/models/data-20.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Recurring",
  "data": {
    "account_vault_id": "account_vault_id6",
    "token_id": "token_id4",
    "contact_id": "contact_id4",
    "account_vault_api_id": "account_vault_api_id4",
    "token_api_id": "token_api_id6",
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

