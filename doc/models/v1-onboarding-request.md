
# V1 Onboarding Request

## Structure

`V1OnboardingRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ParentId` | `string` | Optional | Location ID |
| `PrimaryPrincipal` | [`PrimaryPrincipal1`](../../doc/models/primary-principal-1.md) | Required | The Primary Principal. |
| `TemplateCode` | `string` | Required | The ID of the template to be used - this value will be provided by Fortis.<br><br>**Constraints**: *Maximum Length*: `20`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `Email` | `string` | Required | Merchant email address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `DbaName` | `string` | Required | Merchant 'Doing Business As' name.<br><br>**Constraints**: *Maximum Length*: `100` |
| `Location` | [`Location20`](../../doc/models/location-20.md) | Required | The Location. |
| `AppDelivery` | [`AppDeliveryEnum`](../../doc/models/app-delivery-enum.md) | Required | The delivery method of the app to the merchant.<br><br>**Constraints**: *Maximum Length*: `12` |
| `BusinessCategory` | [`BusinessCategoryEnum?`](../../doc/models/business-category-enum.md) | Optional | The Category of the merchant's business<br><br>> (Required if "business_type" is provided). Note: "business_type" must belong to the appropriate "business_category" |
| `BusinessType` | [`BusinessTypeEnum?`](../../doc/models/business-type-enum.md) | Optional | The Type of a merchant's business. |
| `BusinessDescription` | `string` | Optional | Description of Goods or Services.<br><br>**Constraints**: *Maximum Length*: `200` |
| `SwipedPercent` | `int?` | Optional | Card present/swiped percentage<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `KeyedPercent` | `int?` | Optional | Card not present/keyed percentage<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `EcommercePercent` | `int?` | Optional | eCommerce percentage.<br><br>> The sum total of "swiped_percent", "keyed_percent" and "ecommerce_percent" must add up to 100.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `OwnershipType` | [`OwnershipTypeEnum?`](../../doc/models/ownership-type-enum.md) | Optional | The Ownership Type of the merchant's business.<br><br>**Constraints**: *Maximum Length*: `10` |
| `FedTaxId` | `string` | Optional | Federal Tax ID (EIN).<br><br>**Constraints**: *Maximum Length*: `10` |
| `CcAverageTicketRange` | `int?` | Optional | Average Transaction Amount Range<br><br>> (Applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `CcMonthlyVolumeRange` | `int?` | Optional | Monthly Processing Volume Range<br><br>> (Applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `CcHighTicket` | `int?` | Optional | Highest transaction amount rounded to the next dollar<br><br>> (No decimal and applicable when Template Application Type is 'credit_card' or 'both').<br><br>**Constraints**: `>= 0`, `<= 30000` |
| `EcAverageTicketRange` | `int?` | Optional | Average Transaction Amount Range<br><br>> (Applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `EcMonthlyVolumeRange` | `int?` | Optional | Monthly Processing Volume Range<br><br>> (Applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 1`, `<= 7` |
| `EcHighTicket` | `int?` | Optional | Highest transaction amount rounded to the next dollar<br><br>> (No decimal and applicable when Template Application Type is 'echeck' or 'both').<br><br>**Constraints**: `>= 0`, `<= 30000` |
| `Website` | `string` | Optional | Merchant's business website.<br><br>> (Required if "ecommerce_percent" is greater than 0).<br><br>**Constraints**: *Maximum Length*: `100` |
| `BankAccount` | [`BankAccount`](../../doc/models/bank-account.md) | Optional | The Bank Account. |
| `AltBankAccount` | [`AltBankAccount`](../../doc/models/alt-bank-account.md) | Optional | The Alternative Bank Account. |
| `LegalName` | `string` | Optional | Merchant legal name.<br><br>> (leave blank if same as DBA name).<br><br>**Constraints**: *Maximum Length*: `100` |
| `Contact` | [`Contact11`](../../doc/models/contact-11.md) | Required | The Contact. |
| `ClientAppId` | `string` | Optional | Client Issues Id to track that can be used to track each submitted merchant application. This id should be generated and sent in the request payload, and will be returned in the response payload. If no id is submitted in the payload request, this field will be null in the response.<br><br>**Constraints**: *Maximum Length*: `50` |
| `SecCodes` | [`List<SecCodeEnum>`](../../doc/models/sec-code-enum.md) | Optional | Array of SEC codes that will be allowed, Only applicable for ACH. Valid values are 'PPD', 'WEB', 'TEL', 'CCD'. |

## Example (as JSON)

```json
{
  "primary_principal": {
    "first_name": "Bob",
    "last_name": "Fairview",
    "middle_name": "Nathaniel",
    "title": "Dr",
    "date_of_birth": "2021-12-01",
    "address_line_1": "1354 Oak St.",
    "address_line_2": "Unit 203",
    "city": "Dover",
    "state_province": "DE",
    "postal_code": "55022",
    "ownership_percent": 100,
    "phone_number": "555-555-1234"
  },
  "template_code": "1234YourTemplateCode",
  "email": "email@domain.com",
  "dba_name": "Discount Home Goods",
  "location": {
    "address_line_1": "1200 West Hartford Pkwy",
    "address_line_2": "Suite 2000",
    "city": "Dover",
    "state_province": "DE",
    "postal_code": "55022",
    "phone_number": "555-555-1212"
  },
  "app_delivery": null,
  "business_category": "education",
  "swiped_percent": 0,
  "keyed_percent": 0,
  "ecommerce_percent": 100,
  "ownership_type": "llp",
  "fed_tax_id": "0000000000",
  "cc_average_ticket_range": 5,
  "cc_monthly_volume_range": 1,
  "cc_high_ticket": 1500,
  "ec_average_ticket_range": 5,
  "ec_monthly_volume_range": 2,
  "ec_high_ticket": 1500,
  "website": "http://www.example.com",
  "legal_name": "Total Home Goods, LLP",
  "contact": {
    "first_name": "Jeffery",
    "last_name": "Todd",
    "email": "jtodd@example.com",
    "phone_number": "555-555-3456"
  },
  "client_app_id": "ABC123",
  "parent_id": "parent_id2",
  "business_type": "books_mags_music_and_video",
  "business_description": "business_description0"
}
```

