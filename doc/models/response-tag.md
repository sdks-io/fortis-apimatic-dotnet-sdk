
# Response Tag

*This model accepts additional fields of type object.*

## Structure

`ResponseTag`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type77?`](../../doc/models/type-77.md) | Optional | - |
| `Data` | [`Data22`](../../doc/models/data-22.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Tag",
  "data": {
    "location_id": "location_id4",
    "title": "title6",
    "id": "id0",
    "created_ts": 114,
    "modified_ts": 190,
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

