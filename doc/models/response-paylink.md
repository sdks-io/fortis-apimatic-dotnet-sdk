
# Response Paylink

*This model accepts additional fields of type object.*

## Structure

`ResponsePaylink`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type53?`](../../doc/models/type-53.md) | Optional | - |
| `Data` | [`Data16`](../../doc/models/data-16.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Paylink",
  "data": {
    "location_id": "location_id4",
    "cc_product_transaction_id": "cc_product_transaction_id2",
    "email": "email6",
    "amount_due": 196,
    "location_api_id": "location_api_id0",
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

