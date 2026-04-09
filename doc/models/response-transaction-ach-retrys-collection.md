
# Response Transaction Ach Retrys Collection

## Structure

`ResponseTransactionAchRetrysCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type103Enum?`](../../doc/models/type-103-enum.md) | Optional | Resource Type<br><br>**Default**: `Type103Enum.TransactionAchRetrysCollection` |
| `List` | [`List<List17>`](../../doc/models/list-17.md) | Optional | Resource Members |
| `Links` | [`Links`](../../doc/models/links.md) | Optional | Pagination page links |
| `Pagination` | [`Pagination`](../../doc/models/pagination.md) | Optional | Pagination info |
| `Sort` | [`Sort`](../../doc/models/sort.md) | Optional | Sort information used on the results |

## Example (as JSON)

```json
{
  "type": "TransactionAchRetrysCollection",
  "list": [
    {
      "rejected_transaction_id": "rejected_transaction_id6",
      "return_fee": 150,
      "id": "id2",
      "retry_transaction_id": "retry_transaction_id8",
      "return_fee_transaction_id": "return_fee_transaction_id6"
    },
    {
      "rejected_transaction_id": "rejected_transaction_id6",
      "return_fee": 150,
      "id": "id2",
      "retry_transaction_id": "retry_transaction_id8",
      "return_fee_transaction_id": "return_fee_transaction_id6"
    },
    {
      "rejected_transaction_id": "rejected_transaction_id6",
      "return_fee": 150,
      "id": "id2",
      "retry_transaction_id": "retry_transaction_id8",
      "return_fee_transaction_id": "return_fee_transaction_id6"
    }
  ],
  "links": {
    "type": "Links",
    "first": "first0",
    "previous": "previous2",
    "next": "next2",
    "last": "last4"
  },
  "pagination": {
    "type": "Pagination",
    "total_count": 100,
    "page_count": 212,
    "page_number": 28,
    "page_size": 6
  },
  "sort": {
    "type": "Sorting",
    "fields": [
      {
        "field": "field2",
        "order": "asc"
      },
      {
        "field": "field2",
        "order": "asc"
      },
      {
        "field": "field2",
        "order": "asc"
      }
    ]
  }
}
```

