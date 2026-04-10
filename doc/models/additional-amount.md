
# Additional Amount

*This model accepts additional fields of type object.*

## Structure

`AdditionalAmount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | `object` | Optional | - |
| `Amount` | `int?` | Optional | The amount of additional amount. |
| `AccountType` | `object` | Optional | - |
| `Currency` | `double?` | Optional | Currency Code |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "amount": 10,
  "currency": 840.0,
  "type": {
    "key1": "val1",
    "key2": "val2"
  },
  "account_type": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

