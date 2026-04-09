
# List 11

## Structure

`List11`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AccountVaultId` | `string` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `TokenId` | `string` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ContactId` | `string` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AccountVaultApiId` | `string` | Optional | Token API ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `TokenApiId` | `string` | Optional | Token API ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `Joi` | [`Joi`](../../doc/models/joi.md) | Optional | - |
| `Active` | `bool?` | Optional | Active |
| `Description` | `string` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `36` |
| `EndDate` | `string` | Optional | End date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `InstallmentTotalCount` | `int?` | Optional | Installment Total Count<br><br>**Constraints**: `>= 1`, `<= 999` |
| `Interval` | `int?` | Optional | Interval<br><br>**Constraints**: `>= 0`, `<= 365` |
| `IntervalType` | [`IntervalTypeEnum?`](../../doc/models/interval-type-enum.md) | Optional | Interval Type |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `NotificationDays` | `int?` | Optional | Notification Days<br><br>**Constraints**: `>= 0`, `<= 365` |
| `PaymentMethod` | [`PaymentMethod1Enum?`](../../doc/models/payment-method-1-enum.md) | Optional | Payment Method |
| `ProductTransactionId` | `string` | Optional | Product Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `RecurringId` | `string` | Optional | Recurring ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `RecurringApiId` | `string` | Optional | Recurring Api ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `StartDate` | `string` | Optional | Start date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `Status` | [`StatusEnum?`](../../doc/models/status-enum.md) | Optional | Status |
| `TransactionAmount` | `int?` | Optional | Transaction amount |
| `TermsAgree` | `bool?` | Optional | Terms Agree |
| `TermsAgreeIp` | `string` | Optional | Terms Agree Ip |
| `RecurringC1` | `string` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `RecurringC2` | `string` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `RecurringC3` | `string` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `SendToProcAsRecur` | `bool?` | Optional | Send To Proc As Recur |
| `Tags` | [`List<Tag>`](../../doc/models/tag.md) | Optional | Tag Information on `expand` |
| `SecondaryAmount` | `int?` | Optional | Retained Amount |
| `Currency` | `string` | Optional | - |
| `Id` | `string` | Optional | Recurring ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `NextRunDate` | `string` | Optional | Next Run Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `RecurringTypeId` | [`RecurringTypeIdEnum?`](../../doc/models/recurring-type-id-enum.md) | Optional | Recurring Type |
| `InstallmentAmountTotal` | `int?` | Optional | Installment Amount Total |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `LogEmails` | [`List<LogEmail>`](../../doc/models/log-email.md) | Optional | Log Email Information on `expand` |
| `Contact` | [`Contact1`](../../doc/models/contact-1.md) | Optional | Contact Information on `expand` |
| `AccountVault` | [`AccountVault`](../../doc/models/account-vault.md) | Optional | Token Information on `expand` |
| `CreatedUser` | [`CreatedUser`](../../doc/models/created-user.md) | Optional | User Information on `expand` |
| `Signature` | [`Signature`](../../doc/models/signature.md) | Optional | Signature Information on `expand` |
| `PaymentSchedule` | `List<string>` | Optional | Payment Schedule Information on `expand`<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `Location` | [`Location`](../../doc/models/location.md) | Optional | Location Information on `expand` |
| `ProductTransaction` | [`ProductTransaction`](../../doc/models/product-transaction.md) | Optional | Product Transaction Information on `expand` |
| `NextRunDateMin` | `string` | Optional | Next Run Date Min Information on `expand`<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `NextRunDateMax` | `string` | Optional | Next Run Date Max Information on `expand`<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `AllTags` | [`List<AllTag>`](../../doc/models/all-tag.md) | Optional | All Tag Information on `expand` |
| `Changelogs` | [`List<Changelog>`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `Forecast` | [`Forecast`](../../doc/models/forecast.md) | Optional | Forecast Information on `expand` |
| `RecurringSplits` | [`List<RecurringSplit>`](../../doc/models/recurring-split.md) | Optional | Recurring Split Information on `expand` |

## Example (as JSON)

```json
{
  "account_vault_id": "11e95f8ec39de8fbdb0a4f1a",
  "token_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_vault_api_id": "token1234abcd",
  "token_api_id": "token1234abcd",
  "active": true,
  "description": "Description",
  "end_date": "2021-12-01",
  "installment_total_count": 20,
  "interval": 1,
  "interval_type": "d",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "notification_days": 2,
  "payment_method": "cc",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_api_id": "recurring1234abcd",
  "start_date": "2021-12-01",
  "status": "active",
  "transaction_amount": 300,
  "terms_agree": true,
  "terms_agree_ip": "192.168.0.10",
  "recurring_c1": "recurring custom data 1",
  "recurring_c2": "recurring custom data 2",
  "recurring_c3": "recurring custom data 3",
  "send_to_proc_as_recur": true,
  "secondary_amount": 100,
  "currency": "USD",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "next_run_date": "2021-12-01",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "recurring_type_id": "i",
  "installment_amount_total": 99999999,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "next_run_date_min": "2021-12-01",
  "next_run_date_max": "2021-12-01"
}
```

