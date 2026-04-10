
# Response Transaction Ach Retry

*This model accepts additional fields of type object.*

## Structure

`ResponseTransactionAchRetry`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type99?`](../../doc/models/type-99.md) | Optional | - |
| `Data` | [`Data26`](../../doc/models/data-26.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "TransactionAchRetry",
  "data": {
    "rejected_transaction_id": "rejected_transaction_id4",
    "return_fee": 208,
    "id": "id0",
    "retry_transaction_id": "retry_transaction_id6",
    "return_fee_transaction_id": "return_fee_transaction_id4",
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

