
# Response Three Ds Transaction

*This model accepts additional fields of type object.*

## Structure

`ResponseThreeDsTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type46?`](../../doc/models/type-46.md) | Optional | - |
| `Data` | [`Data13`](../../doc/models/data-13.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ThreeDSTransaction",
  "data": {
    "three_ds_server_trans_id": "three_ds_server_trans_id0",
    "transaction_status": "transaction_status0",
    "ds_trans_id": "ds_trans_id8",
    "acs_trans_id": "acs_trans_id2",
    "message_version": "message_version0",
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

