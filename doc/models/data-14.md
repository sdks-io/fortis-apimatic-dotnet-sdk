
# Data 14

## Structure

`Data14`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | Deposit Id |
| `CompanyId` | `string` | Optional | Company Id |
| `MerchantId` | `string` | Optional | Merchant Id |
| `Service` | `string` | Optional | Service |
| `DepositTypes` | [`List<DepositTypeEnum>`](../../doc/models/deposit-type-enum.md) | Optional | - |
| `DepositAmount` | `double?` | Optional | Deposit Amount |
| `BatchAmount` | `double?` | Optional | Batch Amount |
| `AdjustmentAmount` | `double?` | Optional | Adjustment Amount |
| `RetainedAmount` | `double?` | Optional | Retained Amount |
| `ConveyedAmount` | `double?` | Optional | Conveyed Amount |
| `FeeAmount` | `double?` | Optional | Fee Amount |
| `ReferenceNumber` | `string` | Optional | Reference Number |
| `TraceNumber` | `string` | Optional | - |
| `Currency` | `string` | Optional | Currency |
| `CreatedTs` | `int?` | Optional | Created Timestamp |
| `ReportedDate` | `string` | Optional | Reported Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `TransactionDate` | `string` | Optional | Transaction Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `DepositAccount` | `string` | Optional | Deposit Account |
| `Details` | [`List<Detail2>`](../../doc/models/detail-2.md) | Optional | - |

## Example (as JSON)

```json
{
  "company_id": "8410111",
  "merchant_id": "88441",
  "deposit_amount": 2487.24,
  "batch_amount": 2487.24,
  "adjustment_amount": 2487.24,
  "retained_amount": 2487.24,
  "conveyed_amount": 2487.24,
  "fee_amount": 2487.24,
  "reference_number": "400000",
  "trace_number": "400000",
  "currency": "USD",
  "created_ts": 1422040992,
  "reported_date": "2021-12-01",
  "transaction_date": "2021-12-01",
  "id": "id0",
  "service": "service0",
  "deposit_types": [
    "deposit",
    "adjustment",
    "fee"
  ]
}
```

