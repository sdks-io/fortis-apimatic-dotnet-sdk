
# Balance

*This model accepts additional fields of type object.*

## Structure

`Balance`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AmountType` | `string` | Optional | The type of amount balance |
| `AccountType` | `string` | Optional | The type of account balance |
| `Amount` | `int?` | Optional | The amount of balance |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "amount": 1000,
  "amount_type": "amount_type4",
  "account_type": "account_type6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

