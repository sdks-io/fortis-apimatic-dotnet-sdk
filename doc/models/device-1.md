
# Device 1

*This model accepts additional fields of type object.*

## Structure

`Device1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeviceBindingStatus` | [`DeviceBindingStatus?`](../../doc/models/device-binding-status.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "device_binding_status": "01",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

