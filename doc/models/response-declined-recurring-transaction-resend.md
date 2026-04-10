
# Response Declined Recurring Transaction Resend

*This model accepts additional fields of type object.*

## Structure

`ResponseDeclinedRecurringTransactionResend`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type21?`](../../doc/models/type-21.md) | Optional | - |
| `Data` | [`Data5`](../../doc/models/data-5.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "DeclinedRecurringTransactionResend",
  "data": {
    "id": "id0",
    "email_log_id": "email_log_id2",
    "success": false,
    "email": "email6",
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

