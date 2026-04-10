
# Response User Api Key

*This model accepts additional fields of type object.*

## Structure

`ResponseUserApiKey`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type128?`](../../doc/models/type-128.md) | Optional | - |
| `Data` | [`Data33`](../../doc/models/data-33.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "UserApiKey",
  "data": {
    "user_api_key": "user_api_key2",
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

