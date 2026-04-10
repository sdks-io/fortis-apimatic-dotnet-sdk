
# Batch Risk Config 1

*This model accepts additional fields of type object.*

## Structure

`BatchRiskConfig1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BlindRefundTotalCount` | `int?` | Optional | Blind Refund Total Count<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `BlindRefundMaxAmount` | `int?` | Optional | Blind Refund Max Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "blind_refund_total_count": 66,
  "blind_refund_max_amount": 128,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

