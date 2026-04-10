
# V1 Quick Invoices Request 1

*This model accepts additional fields of type object.*

## Structure

`V1QuickInvoicesRequest1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `CcProductTransactionId` | `string` | Optional | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AchProductTransactionId` | `string` | Optional | ACH Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `DueDate` | `string` | Optional | Due Date, Format: Y-m-d<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `ItemList` | [`List<ItemList5>`](../../doc/models/item-list-5.md) | Optional | Item List<br><br>**Constraints**: *Minimum Items*: `1`, *Maximum Items*: `300`, *Unique Items Required* |
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
| `AmountDue` | `int?` | Optional | Amount Due |
| `NotificationEmail` | `string` | Optional | Notification email<br><br>**Constraints**: *Maximum Length*: `640` |
| `StatusId` | `int?` | Optional | (DEPRECATED) Status Id<br><br>**Constraints**: `>= 0`, `<= 1` |
| `StatusCode` | `int?` | Optional | Status Code<br><br>**Constraints**: `>= 0`, `<= 1` |
| `Note` | `string` | Optional | Note<br><br>**Constraints**: *Maximum Length*: `200` |
| `NotificationDaysBeforeDueDate` | `int?` | Optional | Notification days before due date<br><br>**Constraints**: `>= 0`, `<= 60` |
| `NotificationDaysAfterDueDate` | `int?` | Optional | Notification days after due date<br><br>**Constraints**: `>= 0`, `<= 60` |
| `NotificationOnDueDate` | `bool?` | Optional | Notification on due date |
| `SendTextToPay` | `bool?` | Optional | Send Text To Pay |
| `Files` | [`List<File5>`](../../doc/models/file-5.md) | Optional | Files<br><br>> Maximum of 4 files & maximum size of 5MB per file.<br><br>**Constraints**: *Maximum Items*: `4` |
| `RemainingBalance` | `int?` | Optional | Remaining Balance<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `SinglePaymentMinAmount` | `int?` | Optional | Single Payment Min Amount |
| `SinglePaymentMaxAmount` | `int?` | Optional | Single Payment Max Amount |
| `CellPhone` | `string` | Optional | Cell Phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `Tags` | `List<string>` | Optional | Tags |
| `QuickInvoiceC1` | `string` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `QuickInvoiceC2` | `string` | Optional | Custom field 2 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `QuickInvoiceC3` | `string` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `AutoReopen` | `bool?` | Optional | Auto Reopen. If set to true, a void, refund or detachment of a Transaction Payment will cause the QuickInvoice to be opened again |
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
  "amount_due": 24536,
  "notification_email": "email@domain.com",
  "status_id": 1,
  "status_code": 1,
  "note": "some note",
  "notification_days_before_due_date": 3,
  "notification_days_after_due_date": 7,
  "notification_on_due_date": true,
  "send_text_to_pay": true,
  "remaining_balance": 24536,
  "single_payment_min_amount": 500,
  "single_payment_max_amount": 500000,
  "cell_phone": "3339998822",
  "quick_invoice_c1": "custom-data-1",
  "quick_invoice_c2": "custom-data-2",
  "quick_invoice_c3": "custom-data-3",
  "auto_reopen": true,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

