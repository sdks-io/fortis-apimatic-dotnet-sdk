
# V1 Wallet Provider Apple Pay Validate Merchant Request

*This model accepts additional fields of type object.*

## Structure

`V1WalletProviderApplePayValidateMerchantRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Url` | `string` | Required | Url obtained in the ApplePay button click event. Apple's URL that needs to be called to validate merchant. |
| `MerchantId` | `string` | Required | Merchant ID |
| `DomainName` | `string` | Required | Domain Name |
| `DisplayName` | `string` | Required | Title |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "url": "https://apple-pay-gateway-cert.apple.com/paymentservices/startSession",
  "merchantId": "abc1234",
  "domainName": "website.domain.com",
  "displayName": "Sandwich Market",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

