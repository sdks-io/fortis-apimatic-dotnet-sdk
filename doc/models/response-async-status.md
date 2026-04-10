
# Response Async Status

*This model accepts additional fields of type object.*

## Structure

`ResponseAsyncStatus`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type?`](../../doc/models/type.md) | Optional | - |
| `Data` | [`Data`](../../doc/models/data.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "AsyncStatus",
  "data": {
    "code": "00001e1c-0000-0000-0000-000000000000",
    "type": "type0",
    "id": "id0",
    "progress": 100,
    "error": "error4",
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

