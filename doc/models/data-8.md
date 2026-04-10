
# Data 8

*This model accepts additional fields of type object.*

## Structure

`Data8`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | `object` | Optional | - |
| `DigitalWalletsOnly` | `bool?` | Optional | **Default**: `false` |
| `Methods` | [`List<Method3>`](../../doc/models/method-3.md) | Optional | By default the system will try to offer all the availables payment methods from your account. However, if you need to display only cc or ach only use the corresponding product transaction id.<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `Amount` | `int?` | Optional | The total transaction amount to be charged with the transaction intention. Allowed on the actions: `sale`, `auth-only`, `refund`<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `TaxAmount` | `int?` | Optional | Amount of Sales Tax. If supplied, this amount should be already included in the transaction amount. Allowed on the actions: `sale`, `auth-only`, `refund`<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `SecondaryAmount` | `int?` | Optional | secondary_amount is used as a mechanism for partners to collect platform or SaAs fees at a transaction level. This field is intended for use with ISV integrations not standalone merchant integrations. Allowed on the actions: `sale`, `auth-only`.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ContactId` | `string` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `SaveAccount` | `bool?` | Optional | Specifies to tokenize card/bank information within the transaction. Allowed on the actions: `sale`, `auth-only`, `avs-only`, `refund`. Do not include with `tokeniation` action. |
| `SaveAccountTitle` | `string` | Optional | Specifies to tokenize card/bank information within the transaction. Allowed on the actions: `sale`, `auth-only`, `avs-only`, `refund`. Do not include with `tokeniation` action.<br><br>**Constraints**: *Maximum Length*: `16` |
| `Title` | `string` | Optional | A title for the token.<br><br>**Constraints**: *Maximum Length*: `16` |
| `AchSecCode` | `object` | Optional | - |
| `BankFundedOnlyOverride` | `bool?` | Optional | Bank Funded Only Override. Force the use of a bank funded debit card on debit repayment type transactions. |
| `AllowPartialAuthorizationOverride` | `bool?` | Optional | Allow partial Authorization Override. Must have Fortis approval for production access. |
| `AutoDeclineCvvOverride` | `bool?` | Optional | Auto Decline Cvv Override |
| `AutoDeclineStreetOverride` | `bool?` | Optional | Auto Decline Street Override |
| `AutoDeclineZipOverride` | `bool?` | Optional | Auto Decline Zip Override |
| `Message` | `string` | Optional | A custom text message that displays after the payment is processed.<br><br>**Constraints**: *Maximum Length*: `120` |
| `ClientToken` | `string` | Optional | A JWT to be used to create the elements.<br><br>> This is a one-time only use token.<br>> Do not store for long term use. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "digitalWalletsOnly": false,
  "amount": 1099,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "client_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c",
  "action": {
    "key1": "val1",
    "key2": "val2"
  },
  "methods": [
    {
      "type": "ach",
      "product_transaction_id": "product_transaction_id4",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "type": "ach",
      "product_transaction_id": "product_transaction_id4",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "type": "ach",
      "product_transaction_id": "product_transaction_id4",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "tax_amount": 94,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

