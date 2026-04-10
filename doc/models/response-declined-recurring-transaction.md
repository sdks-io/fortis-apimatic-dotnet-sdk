
# Response Declined Recurring Transaction

*This model accepts additional fields of type object.*

## Structure

`ResponseDeclinedRecurringTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type15?`](../../doc/models/type-15.md) | Optional | - |
| `Data` | [`Data3`](../../doc/models/data-3.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "DeclinedRecurringTransaction",
  "data": {
    "id": "id0",
    "declined_transaction_id": "declined_transaction_id6",
    "payment_transaction_id": "payment_transaction_id4",
    "status": "paid",
    "recurring_id": "recurring_id4",
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

