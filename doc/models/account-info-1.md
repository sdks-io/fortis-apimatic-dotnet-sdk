
# Account Info 1

*This model accepts additional fields of type object.*

## Structure

`AccountInfo1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ChAccAgeInd` | [`ChAccAgeInd?`](../../doc/models/ch-acc-age-ind.md) | Optional | - |
| `ChAccDate` | `string` | Optional | Date converted into UTC that the cardholder opened the account with the 3DS Requestor. Date format = YYYYMMDD. |
| `ChAccChangeInd` | [`ChAccChangeInd?`](../../doc/models/ch-acc-change-ind.md) | Optional | - |
| `ChAccChange` | `string` | Optional | Date converted into UTC that the cardholder's account with the 3DS Requestor was last changed. Including Billing or Shipping address, new payment account, or new user(s) added. Date format = YYYYMMDD. |
| `ChAccPwChangeInd` | [`ChAccPwChangeInd?`](../../doc/models/ch-acc-pw-change-ind.md) | Optional | - |
| `ChAccPwChange` | `string` | Optional | Date converted into UTC that cardholder's account with the 3DS Requestor had a password change or account reset. Date format must be YYYYMMDD. |
| `ShipAddressUsageInd` | [`ShipAddressUsageInd?`](../../doc/models/ship-address-usage-ind.md) | Optional | - |
| `ShipAddressUsage` | `string` | Optional | Date converted into UTC when the shipping address used for this transaction was first used with the 3DS Requestor. Date format must be YYYYMMDD. |
| `TxnActivityDay` | `int?` | Optional | Number of transactions (successful and abandoned) for this cardholder account with the 3DS Requestor across all payment accounts in the previous 24 hours. |
| `TxnActivityYear` | `int?` | Optional | Number of transactions (successful and abandoned) for this cardholder account with the 3DS Requestor across all payment accounts in the previous year. |
| `ProvisionAttemptsDay` | `int?` | Optional | Number of Add Card attempts in the last 24 hours. |
| `NbPurchaseAccount` | `int?` | Optional | Number of purchases with this cardholder account during the previous six months. |
| `SuspiciousAccActivity` | [`SuspiciousAccActivity?`](../../doc/models/suspicious-acc-activity.md) | Optional | - |
| `ShipNameIndicator` | [`ShipNameIndicator?`](../../doc/models/ship-name-indicator.md) | Optional | - |
| `PaymentAccInd` | [`PaymentAccInd?`](../../doc/models/payment-acc-ind.md) | Optional | - |
| `PaymentAccAge` | `string` | Optional | Date converted into UTC that the payment account was enrolled in the cardholder's account with the 3DS Requestor. Date format must be YYYYMMDD. |
| `ChAccReqId` | `string` | Optional | The 3DS Requestor assigned account identifier of the transacting Cardholder. This identifier is a unique representation of the account identifier for the 3DS Requestor and is provided as a String.<br><br>This field is supported in Starting from EMV 3DS 2.3.1 and later.<br><br>**Constraints**: *Maximum Length*: `64` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "ch_acc_date": "20240401",
  "ch_acc_change": "20240401",
  "ch_acc_pw_change": "20240401",
  "ship_address_usage": "20240401",
  "txn_activity_day": 1,
  "txn_activity_year": 1,
  "provision_attempts_day": 1,
  "nb_purchase_account": 1,
  "payment_acc_age": "20240401",
  "ch_acc_age_ind": "01",
  "ch_acc_change_ind": "03",
  "ch_acc_pw_change_ind": "04",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

