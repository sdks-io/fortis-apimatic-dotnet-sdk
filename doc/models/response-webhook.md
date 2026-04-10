
# Response Webhook

*This model accepts additional fields of type object.*

## Structure

`ResponseWebhook`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type138?`](../../doc/models/type-138.md) | Optional | - |
| `Data` | [`Data39`](../../doc/models/data-39.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "basic_auth_username8",
    "basic_auth_password": "basic_auth_password0",
    "expands": "expands2",
    "format": {
      "key1": "val1",
      "key2": "val2"
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

