
# List 10

*This model accepts additional fields of type object.*

## Structure

`List10`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `CcProductTransactionId` | `string` | Optional | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AchProductTransactionId` | `string` | Optional | ACH Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `DueDate` | `string` | Optional | Due Date, Format: Y-m-d<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `ItemList` | [`List<ItemList>`](../../doc/models/item-list.md) | Optional | Item List<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `300`, *Unique Items Required* |
| `AllowOverpayment` | `bool?` | Optional | Allow Overpayment. |
| `BankFundedOnlyOverride` | `bool?` | Optional | Bank Funded Only override |
| `Email` | `string` | Optional | Email<br><br>**Constraints**: *Maximum Length*: `128` |
| `ContactId` | `string` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ContactApiId` | `string` | Optional | Contact API Id<br><br>**Constraints**: *Maximum Length*: `64` |
| `QuickInvoiceApiId` | `string` | Optional | Quick Invoice API Id<br><br>**Constraints**: *Maximum Length*: `64` |
| `CustomerId` | `string` | Optional | Customer Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ExpireDate` | `string` | Optional | Expire Date.<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `AllowPartialPay` | `bool?` | Optional | Allow partial pay |
| `AttachFilesToEmail` | `bool?` | Optional | Attach Files to Email |
| `SendEmail` | `bool?` | Optional | Send Email |
| `InvoiceNumber` | `string` | Optional | Invoice number<br><br>**Constraints**: *Maximum Length*: `64` |
| `ItemHeader` | `string` | Optional | Item Header<br><br>**Constraints**: *Maximum Length*: `250` |
| `ItemFooter` | `string` | Optional | Item footer<br><br>**Constraints**: *Maximum Length*: `250` |
| `AmountDue` | `double?` | Optional | Amount Due |
| `NotificationEmail` | `string` | Optional | Notification email<br><br>**Constraints**: *Maximum Length*: `640` |
| `StatusId` | `object` | Optional | - |
| `StatusCode` | `object` | Optional | - |
| `Note` | `string` | Optional | Note<br><br>**Constraints**: *Maximum Length*: `200` |
| `NotificationDaysBeforeDueDate` | `int?` | Optional | Notification days before due date<br><br>**Constraints**: `>= 0`, `<= 99` |
| `NotificationDaysAfterDueDate` | `int?` | Optional | Notification days after due date<br><br>**Constraints**: `>= 0`, `<= 99` |
| `NotificationOnDueDate` | `bool?` | Optional | Notification on due date |
| `SendTextToPay` | `bool?` | Optional | Send Text To Pay |
| `Files` | [`List<File>`](../../doc/models/file.md) | Optional | File Information on `expand` |
| `RemainingBalance` | `double?` | Optional | Remaining Balance |
| `SinglePaymentMinAmount` | `int?` | Optional | Single Payment Min Amount |
| `SinglePaymentMaxAmount` | `int?` | Optional | Single Payment Max Amount<br><br>**Default**: `999999999` |
| `CellPhone` | `string` | Optional | Cell Phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `Tags` | [`List<Tag>`](../../doc/models/tag.md) | Optional | Tag Information on `expand` |
| `QuickInvoiceC1` | `string` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `QuickInvoiceC2` | `string` | Optional | Custom field 2 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `QuickInvoiceC3` | `string` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `AutoReopen` | `bool?` | Optional | Auto Reopen. If set to true, a void, refund or detachment of a Transaction Payment will cause the QuickInvoice to be opened again |
| `Id` | `string` | Optional | Quick Invoice ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | Created User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | Modified User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Active` | `bool?` | Optional | Active status |
| `PaymentStatusId` | `int?` | Optional | Payment Status Id<br><br>**Constraints**: `>= 1`, `<= 3` |
| `IsActive` | `bool?` | Optional | Register is active |
| `QuickInvoiceSetting` | [`QuickInvoiceSetting1`](../../doc/models/quick-invoice-setting-1.md) | Optional | - |
| `QuickInvoiceViews` | [`List<QuickInvoiceView>`](../../doc/models/quick-invoice-view.md) | Optional | Quick Invoice View Information on `expand` |
| `Location` | [`Location18`](../../doc/models/location-18.md) | Optional | - |
| `CreatedUser` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `ModifiedUser` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `Changelogs` | [`List<Changelog>`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `Contact` | [`Contact3`](../../doc/models/contact-3.md) | Optional | - |
| `LogEmails` | [`List<LogEmail>`](../../doc/models/log-email.md) | Optional | Log Email Information on `expand` |
| `LogSms` | [`LogSms1`](../../doc/models/log-sms-1.md) | Optional | - |
| `Transactions` | [`List<Transaction>`](../../doc/models/transaction.md) | Optional | Transaction Information on `expand` |
| `CcProductTransaction` | [`ProductTransaction1`](../../doc/models/product-transaction-1.md) | Optional | - |
| `AchProductTransaction` | [`ProductTransaction1`](../../doc/models/product-transaction-1.md) | Optional | - |
| `EmailBlacklist` | [`EmailBlacklist1`](../../doc/models/email-blacklist-1.md) | Optional | - |
| `SmsBlacklist` | [`SmsBlacklist1`](../../doc/models/sms-blacklist-1.md) | Optional | - |
| `PaymentUrl` | `string` | Optional | Payment Url Information on `expand` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "title": "My terminal",
  "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "due_date": "2021-12-01",
  "allow_overpayment": true,
  "bank_funded_only_override": true,
  "email": "email@domain.com",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_api_id": "contact12345",
  "quick_invoice_api_id": "quickinvoice12345",
  "customer_id": "11e95f8ec39de8fbdb0a4f1a",
  "expire_date": "2021-12-01",
  "allow_partial_pay": true,
  "attach_files_to_email": true,
  "send_email": true,
  "invoice_number": "invoice12345",
  "item_header": "Quick invoice header sample",
  "item_footer": "Thank you",
  "amount_due": 245.36,
  "notification_email": "email@domain.com",
  "note": "some note",
  "notification_days_before_due_date": 3,
  "notification_days_after_due_date": 7,
  "notification_on_due_date": true,
  "send_text_to_pay": true,
  "remaining_balance": 245.36,
  "single_payment_min_amount": 500,
  "single_payment_max_amount": 500000,
  "cell_phone": "3339998822",
  "quick_invoice_c1": "custom-data-1",
  "quick_invoice_c2": "custom-data-2",
  "quick_invoice_c3": "custom-data-3",
  "auto_reopen": true,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "active": true,
  "payment_status_id": 1,
  "is_active": true,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

