
# Data 9

*This model accepts additional fields of type object.*

## Structure

`Data9`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Result` | [`Result`](../../doc/models/result.md) | Optional | - |
| `Status` | [`Status5`](../../doc/models/status-5.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "result": {
    "client_app_id": "client_app_id2",
    "dba_name": "dba_name4",
    "email": "email0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "status": {
    "response_code": "response_code0",
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

