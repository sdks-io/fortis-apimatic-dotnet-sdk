
# Address 81

Array of merchant addresses.

*This model accepts additional fields of type object.*

## Structure

`Address81`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddressLine1` | `string` | Required | Line 1 of address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `AddressLine2` | `string` | Optional | Line 2 of address.<br><br>**Constraints**: *Maximum Length*: `20` |
| `City` | `string` | Required | City of address.<br><br>**Constraints**: *Maximum Length*: `50` |
| `StateProvince` | `string` | Required | State or province of address.<br><br>**Constraints**: *Maximum Length*: `2` |
| `PostalCode` | `string` | Required | Postal code of address.<br><br>**Constraints**: *Maximum Length*: `10` |
| `CountryCode` | `string` | Required | Country of address.<br><br>**Constraints**: *Maximum Length*: `2` |
| `AddressType` | [`AddressType`](../../doc/models/address-type.md) | Required | **Constraints**: *Maximum Length*: `20` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "address_line_1": "121 E Main",
  "address_line_2": "Apt 707",
  "city": "Dallas",
  "state_province": "TX",
  "postal_code": "75087",
  "country_code": "US",
  "address_type": "corporate",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

