
# Response Merchant Details

## Structure

`ResponseMerchantDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type137Enum?`](../../doc/models/type-137-enum.md) | Optional | Resource Type<br><br>**Default**: `Type137Enum.MerchantDetails` |
| `Data` | [`Data38`](../../doc/models/data-38.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "MerchantDetails",
  "data": {
    "resultCode": false,
    "merchantID": "merchantID8",
    "applePay": false,
    "googlePay": false,
    "applePayDomains": [
      {
        "key1": "val1",
        "key2": "val2"
      }
    ]
  }
}
```

