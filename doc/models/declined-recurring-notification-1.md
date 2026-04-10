
# Declined Recurring Notification 1

*This model accepts additional fields of type object.*

## Structure

`DeclinedRecurringNotification1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `DeclinedTransactionId` | `string` | Optional | Declined Transaction ID |
| `PaymentTransactionId` | `string` | Optional | Payment Transaction ID |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `ModifiedUserId` | `string` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_ts": 1422040992,
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "declined_transaction_id": "declined_transaction_id4",
  "payment_transaction_id": "payment_transaction_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

