
# Data 15

*This model accepts additional fields of type object.*

## Structure

`Data15`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ParentId` | `string` | Optional | Location ID |
| `PrimaryPrincipal` | [`PrimaryPrincipal3`](../../doc/models/primary-principal-3.md) | Optional | - |
| `TemplateCode` | `string` | Optional | The ID of the template to be used - this value will be provided by Fortis.<br><br>**Constraints**: *Maximum Length*: `20`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `Email` | `string` | Optional | Merchant email address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `DbaName` | `string` | Optional | Merchant 'Doing Business As' name.<br><br>**Constraints**: *Maximum Length*: `100` |
| `Location` | [`Location52`](../../doc/models/location-52.md) | Optional | - |
| `AppDelivery` | `string` | Optional | The delivery method of the app to the merchant.<br><br>**Constraints**: *Maximum Length*: `20` |
| `BusinessCategory` | `object` | Optional | - |
| `BusinessType` | `object` | Optional | - |
| `BusinessDescription` | `string` | Optional | Description of Goods or Services.<br><br>**Constraints**: *Maximum Length*: `200` |
| `SwipedPercent` | `int?` | Optional | Card present/swiped percentage<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `KeyedPercent` | `int?` | Optional | Card not present/keyed percentage<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `EcommercePercent` | `int?` | Optional | eCommerce percentage.<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `OwnershipType` | `object` | Optional | - |
| `FedTaxId` | `string` | Optional | Federal Tax ID (EIN).<br><br>**Constraints**: *Maximum Length*: `10` |
| `CcAverageTicketRange` | `int?` | Optional | Average Transaction Amount Range<br><br>> (Applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `CcMonthlyVolumeRange` | `int?` | Optional | Monthly Processing Volume Range<br><br>> (Applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `CcHighTicket` | `int?` | Optional | Highest transaction amount rounded to the next dollar<br><br>> (No decimal and applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 0`, `<= 30000` |
| `EcAverageTicketRange` | `int?` | Optional | Average Transaction Amount Range<br><br>> (Applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `EcMonthlyVolumeRange` | `int?` | Optional | Monthly Processing Volume Range<br><br>> (Applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `EcHighTicket` | `int?` | Optional | Highest transaction amount rounded to the next dollar<br><br>> (No decimal and applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 0`, `<= 30000` |
| `Website` | `string` | Optional | Merchant's business website.<br><br>> (Required if "ecommerce_percent" is greater than 0).<br><br>**Constraints**: *Maximum Length*: `100` |
| `BankAccount` | [`BankAccount3`](../../doc/models/bank-account-3.md) | Optional | - |
| `AltBankAccount` | [`AltBankAccount2`](../../doc/models/alt-bank-account-2.md) | Optional | - |
| `LegalName` | `string` | Optional | Merchant legal name.<br><br>> (leave blank if same as DBA name).<br><br>**Constraints**: *Maximum Length*: `100` |
| `Contact` | [`Contact2`](../../doc/models/contact-2.md) | Optional | - |
| `ClientAppId` | `string` | Optional | Client Issues Id to track that can be used to track each submitted merchant application. This id should be generated and sent in the request payload, and will be returned in the response payload. If no id is submitted in the payload request, this field will be null in the response.<br><br>**Constraints**: *Maximum Length*: `20` |
| `SecCodes` | [`List<SecCode>`](../../doc/models/sec-code.md) | Optional | Array of SEC codes that will be allowed, Only applicable for ACH. Valid values are 'PPD', 'WEB', 'TEL', 'CCD'. |
| `AppLink` | `string` | Optional | A full page or iframeable link, set in the request app_delivery field, that can be used to retrieve and resume the generated merchant application. No link will be returned if app_delivery is direct<br><br>**Constraints**: *Maximum Length*: `400` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "template_code": "1234YourTemplateCode",
  "email": "jtodd@example.com",
  "dba_name": "Discount Home Goods",
  "app_delivery": "link_full_page",
  "swiped_percent": 0,
  "keyed_percent": 0,
  "ecommerce_percent": 100,
  "fed_tax_id": "0000000000",
  "cc_average_ticket_range": 5,
  "cc_monthly_volume_range": 1,
  "cc_high_ticket": 1500,
  "ec_average_ticket_range": 5,
  "ec_monthly_volume_range": 2,
  "ec_high_ticket": 1500,
  "website": "http://www.example.com",
  "legal_name": "Total Home Goods, LLP",
  "client_app_id": "ABC123",
  "app_link": "https://mpa.example.com/signup/123456788",
  "parent_id": "parent_id0",
  "primary_principal": {
    "first_name": "first_name6",
    "last_name": "last_name4",
    "middle_name": "middle_name6",
    "title": "title2",
    "date_of_birth": "date_of_birth2",
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

