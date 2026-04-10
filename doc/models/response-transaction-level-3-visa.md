
# Response Transaction Level 3 Visa

*This model accepts additional fields of type object.*

## Structure

`ResponseTransactionLevel3Visa`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type115?`](../../doc/models/type-115.md) | Optional | - |
| `Data` | [`Data29`](../../doc/models/data-29.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "TransactionLevel3Visa",
  "data": {
    "id": "id0",
    "transaction_id": "transaction_id8",
    "level3_data": {
      "destination_country_code": "destination_country_code4",
      "duty_amount": 182,
      "freight_amount": 60,
      "national_tax": 999999998900,
      "sales_tax": 999999998900,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
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

