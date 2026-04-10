
# File 5

*This model accepts additional fields of type object.*

## Structure

`File5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FileName` | `string` | Optional | The file name including the extension |
| `Content` | `string` | Optional | File contents as a base64 encoded string |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "file_name": "file_name6",
  "content": "content6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

