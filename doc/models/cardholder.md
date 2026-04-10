
# Cardholder

Contains information for the Cardholder. This field is required unless market or regional mandate restricts sending this information.

*This model accepts additional fields of type object.*

## Structure

`Cardholder`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddressMatch` | [`AddressMatch?`](../../doc/models/address-match.md) | Optional | - |
| `BillingAddress` | [`BillingAddress13`](../../doc/models/billing-address-13.md) | Optional | - |
| `Email` | `string` | Optional | The email address associated with the account that is either entered by the Cardholder, or is on file with the 3DS Requestor. This field shall meet requirements of Section 3.4 of IETF RFC 5322.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `256` |
| `HomePhone` | [`HomePhone2`](../../doc/models/home-phone-2.md) | Optional | - |
| `MobilePhone` | [`MobilePhone2`](../../doc/models/mobile-phone-2.md) | Optional | - |
| `WorkPhone` | [`WorkPhone2`](../../doc/models/work-phone-2.md) | Optional | - |
| `CardholderName` | `string` | Optional | Name of the Cardholder.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `45` |
| `ShippingAddress` | [`ShippingAddress2`](../../doc/models/shipping-address-2.md) | Optional | - |
| `TaxId` | `string` | Optional | Tax ID is the Cardholder's tax identification.<br><br>This field is required depending on the rules provided by the Directory Server.<br>Available for supporting EMV 3DS 2.3.1 and later versions.<br><br>**Constraints**: *Maximum Length*: `45` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "email": "fortis@example.com",
  "cardholder_name": "John Doe",
  "address_match": "Y",
  "billing_address": {
    "city": "city2",
    "country_code": "country_code8",
    "address_line_1": "address_line_12",
    "address_line_2": "address_line_28",
    "address_line_3": "address_line_34",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "home_phone": {
    "cc": "cc8",
    "subscriber": "subscriber0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "mobile_phone": {
    "cc": "cc8",
    "subscriber": "subscriber0",
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

