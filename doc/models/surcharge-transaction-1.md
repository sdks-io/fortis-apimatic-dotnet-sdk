
# Surcharge Transaction 1

*This model accepts additional fields of type object.*

## Structure

`SurchargeTransaction1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModelName` | `string` | Optional | Model Name |
| `TransactionId` | `string` | Optional | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `SurchargeFee` | `int?` | Optional | Surcharge Fee<br><br>**Constraints**: `>= 0` |
| `SurchargeRate` | `int?` | Optional | Surcharge Rate<br><br>**Constraints**: `>= 0` |
| `SurchargeAmount` | `int?` | Optional | Surcharge Amount<br><br>**Constraints**: `>= 0` |
| `SurchargeTransactionMin` | `int?` | Optional | Surcharge Transaction Minimum<br><br>**Constraints**: `>= 0` |
| `SurchargeTransactionMax` | `int?` | Optional | Surcharge Transaction Maximum<br><br>**Constraints**: `>= 0` |
| `Created` | `int?` | Optional | Created |
| `Modified` | `int?` | Optional | Modified |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "model_name": "Model Name",
  "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "surcharge_fee": 0,
  "surcharge_rate": 0,
  "created": 1422040992,
  "modified": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

