
# Bank Account 1

Array of bank account objects.

> One account with “deposit_type” of primary is required. Maximum of two accounts are allowed.

*This model accepts additional fields of type object.*

## Structure

`BankAccount1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AccountHolderName` | `string` | Required | Account holder name.<br><br>**Constraints**: *Maximum Length*: `40` |
| `RoutingNumber` | `string` | Required | Nine-digit Bank routing number.<br><br>**Constraints**: *Maximum Length*: `9` |
| `AccountNumber` | `string` | Required | Account number.<br><br>**Constraints**: *Maximum Length*: `17` |
| `IsPrimary` | `bool?` | Optional | Flag indicating whether or not the account is the primary account. Only one account can be marked as primary.<br><br>> Indicates that the account should be the primary account for the merchant. One and only one account may be set to true. |
| `AccountType` | [`AccountType12`](../../doc/models/account-type-12.md) | Required | **Constraints**: *Maximum Length*: `10` |
| `AltDepositTypes` | `List<string>` | Optional | Array of deposit types. ('fees', 'adjustments', 'returns') |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "account_holder_name": "James Bond",
  "routing_number": "111111111",
  "account_number": "1234567",
  "is_primary": true,
  "account_type": "checking",
  "alt_deposit_types": [
    "alt_deposit_types0",
    "alt_deposit_types9"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

