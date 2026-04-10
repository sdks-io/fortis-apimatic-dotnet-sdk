
# Device

Contains device information.

Available for supporting EMV 3DS 2.3.1 and later versions.

*This model accepts additional fields of type object.*

## Structure

`Device`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DeviceBindingStatus` | [`DeviceBindingStatus?`](../../doc/models/device-binding-status.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "device_binding_status": "38",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

