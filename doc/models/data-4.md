
# Data 4

## Structure

`Data4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeclinedRecurringTransactionId` | `string` | Optional | Declined Recurring Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AccountNumber` | `string` | Optional | Account Number<br><br>**Constraints**: *Minimum Length*: `13`, *Maximum Length*: `19` |
| `AccountHolderName` | `string` | Optional | Account Holder Name |
| `ExpDate` | `string` | Optional | Exp Date<br><br>**Constraints**: *Maximum Length*: `4` |
| `TransactionAmount` | `int?` | Optional | Transaction Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `Description` | `string` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `255` |
| `BillingAddress` | [`BillingAddress`](../../doc/models/billing-address.md) | Optional | Billing Address Object |
| `Tags` | `List<string>` | Optional | Tags |
| `Id` | `string` | Optional | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `FirstSix` | `string` | Optional | First Six<br><br>**Constraints**: *Maximum Length*: `6` |
| `LastFour` | `string` | Optional | Last Four<br><br>**Constraints**: *Maximum Length*: `4` |
| `Routing` | `string` | Optional | Routing |
| `StatusId` | `double?` | Optional | Status Id |
| `ReasonCodeId` | [`ReasonCodeIdEnum?`](../../doc/models/reason-code-id-enum.md) | Optional | Reason Code Id |
| `TypeId` | `double?` | Optional | Type Id |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "declined_recurring_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_number": "5454545454545454",
  "account_holder_name": "John Doe",
  "exp_date": "0722",
  "transaction_amount": 0,
  "description": "Description",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "first_six": "700953",
  "last_four": "3657",
  "reason_code_id": 1000,
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a"
}
```

