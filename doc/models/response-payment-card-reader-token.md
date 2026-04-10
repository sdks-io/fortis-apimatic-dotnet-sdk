
# Response Payment Card Reader Token

*This model accepts additional fields of type object.*

## Structure

`ResponsePaymentCardReaderToken`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type58?`](../../doc/models/type-58.md) | Optional | - |
| `Data` | [`Data17`](../../doc/models/data-17.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "PaymentCardReaderToken",
  "data": {
    "token": "token4",
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

