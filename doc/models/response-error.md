
# Response Error

*This model accepts additional fields of type object.*

## Structure

`ResponseError`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | `string` | Optional | Message type |
| `Id` | `string` | Optional | Unique identifier for this API call |
| `StatusCode` | `int?` | Optional | HTTP status code |
| `Title` | `string` | Optional | Error title |
| `Detail` | [`Detail12`](../../doc/models/detail-12.md) | Optional | - |
| `Meta` | `object` | Optional | Object with additional error details |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Error",
  "id": "c7f03d44-c966-4578-93ff-295f3ef6a467",
  "statusCode": 400,
  "title": "Bad Request",
  "detail": {
    "three_ds_server_trans_id": "three_ds_server_trans_id6",
    "acs_trans_id": "acs_trans_id8",
    "ds_trans_id": "ds_trans_id4",
    "error_code": "error_code4",
    "error_component": "error_component2",
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

