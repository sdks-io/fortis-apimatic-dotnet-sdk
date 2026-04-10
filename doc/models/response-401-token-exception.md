
# Response 401 Token Exception

*This model accepts additional fields of type object.*

## Structure

`Response401TokenException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatusCode` | `int?` | Optional | Response code |
| `Error` | `string` | Optional | Unauthorized |
| `Message` | `string` | Optional | Invalid token |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "statusCode": 401,
  "error": "Unauthorized",
  "message": "Invalid token",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

