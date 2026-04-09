
# V1 Elements Transaction Intention Request

## Structure

`V1ElementsTransactionIntentionRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`ActionEnum?`](../../doc/models/action-enum.md) | Optional | The transaction action to be performed with the transaction intention. `sale`, `auth-only`, `avs-only`, `tokenization`.<br><br>**Default**: `ActionEnum.sale` |
| `DigitalWalletsOnly` | `bool?` | Optional | **Default**: `false` |
| `Methods` | [`List<Method50>`](../../doc/models/method-50.md) | Optional | By default the system will try to offer all the availables payment methods from your account. However, if you need to display only cc or ach only use the corresponding product transaction id.<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `Amount` | `int?` | Optional | The total transaction amount to be charged with the transaction intention. Allowed on the actions: `sale`, `auth-only`, `refund`<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `TaxAmount` | [`V1ElementsTransactionIntentionRequestTaxAmount`](../../doc/models/containers/v1-elements-transaction-intention-request-tax-amount.md) | Optional | This is a container for any-of cases.<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `SecondaryAmount` | [`V1ElementsTransactionIntentionRequestSecondaryAmount`](../../doc/models/containers/v1-elements-transaction-intention-request-secondary-amount.md) | Optional | This is a container for any-of cases.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ContactId` | `string` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `SaveAccount` | [`V1ElementsTransactionIntentionRequestSaveAccount`](../../doc/models/containers/v1-elements-transaction-intention-request-save-account.md) | Optional | This is a container for any-of cases. |
| `SaveAccountTitle` | [`V1ElementsTransactionIntentionRequestSaveAccountTitle`](../../doc/models/containers/v1-elements-transaction-intention-request-save-account-title.md) | Optional | This is a container for any-of cases.<br><br>**Constraints**: *Maximum Length*: `16` |
| `Title` | [`V1ElementsTransactionIntentionRequestTitle`](../../doc/models/containers/v1-elements-transaction-intention-request-title.md) | Optional | This is a container for any-of cases.<br><br>**Constraints**: *Maximum Length*: `16` |
| `AchSecCode` | [`AchSecCodeEnum?`](../../doc/models/ach-sec-code-enum.md) | Optional | SEC code for the transaction if it's an ACH transaction.<br><br>**Default**: `AchSecCodeEnum.WEB` |
| `BankFundedOnlyOverride` | [`V1ElementsTransactionIntentionRequestBankFundedOnlyOverride`](../../doc/models/containers/v1-elements-transaction-intention-request-bank-funded-only-override.md) | Optional | This is a container for any-of cases. |
| `AllowPartialAuthorizationOverride` | [`V1ElementsTransactionIntentionRequestAllowPartialAuthorizationOverride`](../../doc/models/containers/v1-elements-transaction-intention-request-allow-partial-authorization-override.md) | Optional | This is a container for any-of cases. |
| `AutoDeclineCvvOverride` | [`V1ElementsTransactionIntentionRequestAutoDeclineCvvOverride`](../../doc/models/containers/v1-elements-transaction-intention-request-auto-decline-cvv-override.md) | Optional | This is a container for any-of cases. |
| `AutoDeclineStreetOverride` | [`V1ElementsTransactionIntentionRequestAutoDeclineStreetOverride`](../../doc/models/containers/v1-elements-transaction-intention-request-auto-decline-street-override.md) | Optional | This is a container for any-of cases. |
| `AutoDeclineZipOverride` | [`V1ElementsTransactionIntentionRequestAutoDeclineZipOverride`](../../doc/models/containers/v1-elements-transaction-intention-request-auto-decline-zip-override.md) | Optional | This is a container for any-of cases. |
| `Message` | `string` | Optional | A custom text message that displays after the payment is processed.<br><br>**Constraints**: *Maximum Length*: `120` |

## Example (as JSON)

```json
{
  "action": "sale",
  "digitalWalletsOnly": false,
  "amount": 1099,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "ach_sec_code": "WEB",
  "methods": [
    {
      "type": "ach",
      "product_transaction_id": "product_transaction_id4"
    }
  ],
  "tax_amount": 50
}
```

