
# Response Send Verification

*This model accepts additional fields of type object.*

## Structure

`ResponseSendVerification`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type135?`](../../doc/models/type-135.md) | Optional | - |
| `Data` | [`Data32`](../../doc/models/data-32.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "SendVerification",
  "data": {
    "id": "id0",
    "user_id": "user_id8",
    "hash": "hash6",
    "created_ts": 114,
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

