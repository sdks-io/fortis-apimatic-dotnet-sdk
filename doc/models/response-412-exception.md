
# Response 412 Exception

*This model accepts additional fields of type object.*

## Structure

`Response412Exception`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | `string` | Optional | - |
| `Id` | `string` | Optional | - |
| `StatusCode` | `int?` | Optional | Response code |
| `Title` | `string` | Optional | Error description |
| `Detail` | `string` | Optional | Error details |
| `Meta` | [`Meta`](../../doc/models/meta.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "clj4ge1234004t9ptdoz34567",
  "id": "clj4ge1234004t9ptdoz34567",
  "statusCode": 412,
  "title": "Precondition Failed",
  "detail": "\"fieldName\" is required",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

