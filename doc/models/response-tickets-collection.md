
# Response Tickets Collection

*This model accepts additional fields of type object.*

## Structure

`ResponseTicketsCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type88?`](../../doc/models/type-88.md) | Optional | - |
| `List` | [`List<List15>`](../../doc/models/list-15.md) | Optional | Resource Members |
| `Links` | [`Links1`](../../doc/models/links-1.md) | Optional | - |
| `Pagination` | [`Pagination1`](../../doc/models/pagination-1.md) | Optional | - |
| `Sort` | [`Sort1`](../../doc/models/sort-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "TicketsCollection",
  "list": [
    {
      "account_holder_name": "account_holder_name8",
      "exp_date": "exp_date0",
      "cvv": "cvv0",
      "account_number": "account_number2",
      "billing_address": {
        "postal_code": "postal_code0",
        "street": "street8",
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
      "account_holder_name": "account_holder_name8",
      "exp_date": "exp_date0",
      "cvv": "cvv0",
      "account_number": "account_number2",
      "billing_address": {
        "postal_code": "postal_code0",
        "street": "street8",
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
      "account_holder_name": "account_holder_name8",
      "exp_date": "exp_date0",
      "cvv": "cvv0",
      "account_number": "account_number2",
      "billing_address": {
        "postal_code": "postal_code0",
        "street": "street8",
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

