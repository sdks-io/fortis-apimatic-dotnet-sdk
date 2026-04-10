
# Links

Pagination page links

*This model accepts additional fields of type object.*

## Structure

`Links`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type2?`](../../doc/models/type-2.md) | Optional | - |
| `First` | `string` | Optional | Link to the first page |
| `Previous` | `string` | Optional | Link to the previous page |
| `Next` | `string` | Optional | Link to the next page |
| `Last` | `string` | Optional | Link to the last page |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "first": "/v1/endpoint?page[size]=10&page[number]=1",
  "previous": "/v1/endpoint?page[size]=10&page[number]=5",
  "next": "/v1/endpoint?page[size]=10&page[number]=7",
  "last": "/v1/endpoint?page[size]=10&page[number]=42",
  "type": "Links",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

