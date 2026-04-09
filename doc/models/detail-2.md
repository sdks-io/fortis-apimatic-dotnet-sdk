
# Detail 2

## Structure

`Detail2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ProcessorBatchNumber` | `string` | Optional | Processor Batch Number |
| `ProductCode` | `string` | Optional | Product Code |
| `DepositDetailType` | `string` | Optional | Deposit Detail Type |
| `Amount` | `double?` | Optional | Amount |
| `Memo` | `string` | Optional | Memo |
| `ReportedDate` | `string` | Optional | Reported Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `SettledDate` | `string` | Optional | Settled Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `Mid` | `string` | Optional | Merchant ID |

## Example (as JSON)

```json
{
  "amount": 2487.24,
  "reported_date": "2021-12-01",
  "settled_date": "2021-12-01",
  "processor_batch_number": "processor_batch_number6",
  "product_code": "product_code8",
  "deposit_detail_type": "deposit_detail_type6",
  "memo": "memo6"
}
```

