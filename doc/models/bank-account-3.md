
# Bank Account 3

*This model accepts additional fields of type object.*

## Structure

`BankAccount3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RoutingNumber` | `string` | Optional | Nine-digit Bank routing number.<br><br>**Constraints**: *Maximum Length*: `9` |
| `AccountNumber` | `string` | Optional | Bank account number.<br><br>**Constraints**: *Maximum Length*: `17` |
| `AccountHolderName` | `string` | Optional | Name on bank account.<br><br>**Constraints**: *Maximum Length*: `40` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "routing_number": "011103093",
  "account_number": "01234567890123",
  "account_holder_name": "Bob Fairview",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

