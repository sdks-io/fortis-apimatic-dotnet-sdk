
# Response Apple Pay Validate Merchant

*This model accepts additional fields of type object.*

## Structure

`ResponseApplePayValidateMerchant`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type136?`](../../doc/models/type-136.md) | Optional | - |
| `Data` | [`Data37`](../../doc/models/data-37.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ApplePayValidateMerchant",
  "data": {
    "merchantSession": "merchantSession0",
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

