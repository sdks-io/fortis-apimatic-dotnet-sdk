
# List 17

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
| `RejectedTransaction` | [`RejectedTransaction`](../../doc/models/rejected-transaction.md) | Optional | Transaction Information on `expand` |
| `RetryTransaction` | [`RetryTransaction`](../../doc/models/retry-transaction.md) | Optional | Transaction Information on `expand` |
| `ReturnFeeTransaction` | [`ReturnFeeTransaction`](../../doc/models/return-fee-transaction.md) | Optional | Transaction Information on `expand` |
| `CreatedUser` | [`CreatedUser`](../../doc/models/created-user.md) | Optional | User Information on `expand` |
| `Changelogs` | [`List<Changelog>`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |

## Example (as JSON)

```json
{
  "rejected_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "retry_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "return_fee_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "return_fee": 230
}
```

