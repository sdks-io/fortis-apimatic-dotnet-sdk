
# Meta

*This model accepts additional fields of type object.*

## Structure

`Meta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Details` | [`List<Detail>`](../../doc/models/detail.md) | Optional | Error detail |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "details": [
    {
      "message": "message0",
      "path": [
        "path6"
      ],
      "type": "type0",
      "context": {
        "key": "key2",
        "label": "label2",
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
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

