
# Surcharge 1

*This model accepts additional fields of type object.*

## Structure

`Surcharge1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SurchargeFee` | `int?` | Optional | Surcharge Fee |
| `SurchargeRate` | `int?` | Optional | Surcharge Rate |
| `MaxTransactionAmount` | `int?` | Optional | Max Transaction Amount |
| `MinFeeAmount` | `int?` | Optional | Min Fee Amount |
| `MaxFeeAmount` | `int?` | Optional | Max Fee Amount |
| `SurchargeOnRecurring` | `bool?` | Optional | Surcharge On Recurring |
| `RefundSurcharges` | `bool?` | Optional | Refund Surcharges |
| `BlindRefundSurcharges` | `bool?` | Optional | Blind Refund Surcharges |
| `ProductTransactionId` | `string` | Optional | Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `RunAsSeparateTransaction` | `bool?` | Optional | Run As Separate Transaction |
| `ApplyToUserTypeId` | `string` | Optional | Apply To User Type Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `256` |
| `SurchargeLabel` | `string` | Optional | Surcharge Label<br><br>**Constraints**: *Maximum Length*: `64` |
| `SurchargeTransactionProductId` | `string` | Optional | Surcharge Transaction Product Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `StateExceptionCheck` | `bool?` | Optional | State Exception Check |
| `Compliant` | `bool?` | Optional | Compliant |
| `Id` | `string` | Optional | Surcharge Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "surcharge_fee": 10,
  "surcharge_rate": 1,
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "apply_to_user_type_id": "11e95f8ec39de8fbdb0a4f1a",
  "surcharge_transaction_product_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "max_transaction_amount": 82,
  "min_fee_amount": 28,
  "max_fee_amount": 2,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

