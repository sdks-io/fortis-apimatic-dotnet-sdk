
# Pagination

Pagination info

*This model accepts additional fields of type object.*

## Structure

`Pagination`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type3?`](../../doc/models/type-3.md) | Optional | - |
| `TotalCount` | `int?` | Optional | Total records count |
| `PageCount` | `int?` | Optional | Total page count |
| `PageNumber` | `int?` | Optional | Current page |
| `PageSize` | `int?` | Optional | Page size |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "total_count": 423,
  "page_count": 42,
  "page_number": 6,
  "page_size": 10,
  "type": "Pagination",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

