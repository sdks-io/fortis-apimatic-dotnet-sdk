
# List 17

*This model accepts additional fields of type object.*

## Structure

`List17`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RejectedTransactionId` | `string` | Optional | Rejected Transaction ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ReturnFee` | `int?` | Optional | Return Fee.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `Id` | `string` | Optional | Transaction ACH Retry ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `RetryTransactionId` | `string` | Optional | Retry Transaction ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ReturnFeeTransactionId` | `string` | Optional | Return Fee Transaction ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `RejectedTransaction` | [`Transaction`](../../doc/models/transaction.md) | Optional | - |
| `RetryTransaction` | [`Transaction`](../../doc/models/transaction.md) | Optional | - |
| `ReturnFeeTransaction` | [`Transaction`](../../doc/models/transaction.md) | Optional | - |
| `CreatedUser` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `Changelogs` | [`List<Changelog>`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "rejected_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "retry_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "return_fee_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "return_fee": 230,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

