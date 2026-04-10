
# Transaction Batch

Transaction Batch Information on `expand`

*This model accepts additional fields of type object.*

## Structure

`TransactionBatch`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | Batch ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ProductTransactionId` | `string` | Optional | Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ProcessingStatusId` | `int?` | Optional | Processing Status Id<br><br>**Constraints**: `>= 1`, `<= 5` |
| `BatchNum` | `int?` | Optional | Batch Number |
| `IsOpen` | `double?` | Optional | 1 = Batch is_open, 0 = Batch is closed. Only 1 open batch per product_transaction_id.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `SettlementFileName` | `string` | Optional | Settlement File Name |
| `BatchCloseTs` | `double?` | Optional | Batch Close Ts in unix |
| `BatchCloseDetail` | `string` | Optional | Batch Close Detail |
| `TotalSaleAmount` | `int?` | Optional | Total Sale Amount |
| `TotalSaleCount` | `int?` | Optional | Total Sale Count |
| `TotalRefundAmount` | `int?` | Optional | Total Refund Amount |
| `TotalRefundCount` | `int?` | Optional | Total Refund Count |
| `TotalVoidAmount` | `int?` | Optional | Total Void Amount |
| `TotalVoidCount` | `int?` | Optional | Total Void Count |
| `TotalBlindRefundAmount` | `int?` | Optional | Total Blind Refund Amount |
| `TotalBlindRefundCount` | `int?` | Optional | Total Blind Refund Count |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "processing_status_id": 2,
  "batch_num": 4,
  "is_open": 0,
  "settlement_file_name": "settement_file.txt",
  "batch_close_ts": 1531423693,
  "batch_close_detail": "BATCH_MISMATCH",
  "total_sale_amount": 2342,
  "total_sale_count": 21,
  "total_refund_amount": 2342,
  "total_refund_count": 18,
  "total_void_amount": 2342,
  "total_void_count": 17,
  "total_blind_refund_amount": 2342,
  "total_blind_refund_count": 16,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

