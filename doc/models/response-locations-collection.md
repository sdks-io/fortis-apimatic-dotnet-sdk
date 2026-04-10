
# Response Locations Collection

*This model accepts additional fields of type object.*

## Structure

`ResponseLocationsCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type35?`](../../doc/models/type-35.md) | Optional | - |
| `List` | [`List<List6>`](../../doc/models/list-6.md) | Optional | Resource Members |
| `Links` | [`Links1`](../../doc/models/links-1.md) | Optional | - |
| `Pagination` | [`Pagination1`](../../doc/models/pagination-1.md) | Optional | - |
| `Sort` | [`Sort1`](../../doc/models/sort-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "LocationsCollection",
  "list": [
    {
      "id": "id2",
      "created_ts": 56,
      "modified_ts": 124,
      "account_number": "account_number2",
      "address": {
        "city": "city6",
        "state": "state2",
        "postal_code": "postal_code8",
        "country": {
          "key1": "val1",
          "key2": "val2"
        },
        "street": "street6",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "id": "id2",
      "created_ts": 56,
      "modified_ts": 124,
      "account_number": "account_number2",
      "address": {
        "city": "city6",
        "state": "state2",
        "postal_code": "postal_code8",
        "country": {
          "key1": "val1",
          "key2": "val2"
        },
        "street": "street6",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "id": "id2",
      "created_ts": 56,
      "modified_ts": 124,
      "account_number": "account_number2",
      "address": {
        "city": "city6",
        "state": "state2",
        "postal_code": "postal_code8",
        "country": {
          "key1": "val1",
          "key2": "val2"
        },
        "street": "street6",
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

