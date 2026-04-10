
# Response Paylinks Collection

*This model accepts additional fields of type object.*

## Structure

`ResponsePaylinksCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type54?`](../../doc/models/type-54.md) | Optional | - |
| `List` | [`List<List9>`](../../doc/models/list-9.md) | Optional | Resource Members |
| `Links` | [`Links1`](../../doc/models/links-1.md) | Optional | - |
| `Pagination` | [`Pagination1`](../../doc/models/pagination-1.md) | Optional | - |
| `Sort` | [`Sort1`](../../doc/models/sort-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "PaylinksCollection",
  "list": [
    {
      "location_id": "location_id6",
      "cc_product_transaction_id": "cc_product_transaction_id6",
      "email": "email4",
      "amount_due": 138,
      "location_api_id": "location_api_id2",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "location_id": "location_id6",
      "cc_product_transaction_id": "cc_product_transaction_id6",
      "email": "email4",
      "amount_due": 138,
      "location_api_id": "location_api_id2",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "links": {
    "type": "Links",
    "first": "first0",
    "previous": "previous2",
    "next": "next2",
    "last": "last4",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "pagination": {
    "type": "Pagination",
    "total_count": 100,
    "page_count": 212,
    "page_number": 28,
    "page_size": 6,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "sort": {
    "type": "Sorting",
    "fields": [
      {
        "field": "field2",
        "order": "asc",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "field": "field2",
        "order": "asc",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "field": "field2",
        "order": "asc",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

