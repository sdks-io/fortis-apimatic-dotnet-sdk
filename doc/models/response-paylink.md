
# Response Paylink

## Structure

`ResponsePaylink`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type53Enum?`](../../doc/models/type-53-enum.md) | Optional | Resource Type<br><br>**Default**: `Type53Enum.Paylink` |
| `Data` | [`Data16`](../../doc/models/data-16.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "Paylink",
  "data": {
    "location_id": "location_id4",
    "cc_product_transaction_id": "cc_product_transaction_id2",
    "email": "email6",
    "amount_due": 196,
    "location_api_id": "location_api_id0"
  }
}
```

