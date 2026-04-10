
# Response Three Ds Authentication

*This model accepts additional fields of type object.*

## Structure

`ResponseThreeDsAuthentication`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type45?`](../../doc/models/type-45.md) | Optional | - |
| `Data` | [`Data12`](../../doc/models/data-12.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ThreeDSAuthentication",
  "data": {
    "three_ds_server_trans_id": "three_ds_server_trans_id0",
    "acs_url": "acs_url2",
    "transaction_status": "D",
    "authentication_value": "authentication_value2",
    "eci": "eci0",
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

