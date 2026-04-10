
# Billing Address 24

Cardholder billing address object

*This model accepts additional fields of type object.*

## Structure

`BillingAddress24`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `City` | `string` | Optional | The city of the Cardholder billing address associated with the card used for this purchase.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `50` |
| `CountryCode` | `string` | Optional | The ISO 3166-1 alpha-3 or alpha-2 country of the Cardholder billing address associated with the card used for this purchase.<br><br>The field is required if Cardholder Billing Address State is present and unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `3` |
| `AddressLine1` | `string` | Optional | First line of the street address or equivalent local portion of the Cardholder billing address associated with the card use for this purchase.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `50` |
| `AddressLine2` | `string` | Optional | Second line of the street address or equivalent local portion of the Cardholder billing address associated with the card use for this purchase.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `50` |
| `AddressLine3` | `string` | Optional | Third line of the street address or equivalent local portion of the Cardholder billing address associated with the card use for this purchase.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `50` |
| `PostalCode` | `string` | Optional | ZIP or other postal code of the Cardholder billing address associated with the card used for this purchase.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `16` |
| `State` | `string` | Optional | The state or province of the Cardholder billing address associated with the card used for this purchase. The value should be the country subdivision code defined in ISO 3166-2.<br><br>This field is required unless State is not applicable for this country and unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `3` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "city": "Plano",
  "country_code": "USA",
  "address_line_1": "6111 W Plano Parkway",
  "address_line_2": "Suite 2700",
  "postal_code": "75093",
  "state": "TX",
  "address_line_3": "address_line_30",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

