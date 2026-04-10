
# Response Signatures Collection

*This model accepts additional fields of type object.*

## Structure

`ResponseSignaturesCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type73?`](../../doc/models/type-73.md) | Optional | - |
| `List` | [`List<List12>`](../../doc/models/list-12.md) | Optional | Resource Members |
| `Links` | [`Links1`](../../doc/models/links-1.md) | Optional | - |
| `Pagination` | [`Pagination1`](../../doc/models/pagination-1.md) | Optional | - |
| `Sort` | [`Sort1`](../../doc/models/sort-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "SignaturesCollection",
  "list": [
    {
      "signature": "signature0",
      "resource": "Recurring",
      "resource_id": "resource_id8",
      "id": "id2",
      "created_ts": 56,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "signature": "signature0",
      "resource": "Recurring",
      "resource_id": "resource_id8",
      "id": "id2",
      "created_ts": 56,
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

