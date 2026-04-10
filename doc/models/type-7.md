
# Type 7

*This model accepts additional fields of type object.*

## Structure

`Type7`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int?` | Optional | ID |
| `Title` | `string` | Optional | Title |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": 50,
  "title": "Sample Title",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

