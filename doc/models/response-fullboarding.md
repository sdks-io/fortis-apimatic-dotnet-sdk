
# Response Fullboarding

*This model accepts additional fields of type object.*

## Structure

`ResponseFullboarding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type30?`](../../doc/models/type-30.md) | Optional | - |
| `Data` | [`Data9`](../../doc/models/data-9.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Fullboarding",
  "data": {
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
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

