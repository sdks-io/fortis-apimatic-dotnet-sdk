
# Sort 1

*This model accepts additional fields of type object.*

## Structure

`Sort1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type4?`](../../doc/models/type-4.md) | Optional | - |
| `Fields` | [`List<Field>`](../../doc/models/field.md) | Optional | [object Object] |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
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
    }
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

