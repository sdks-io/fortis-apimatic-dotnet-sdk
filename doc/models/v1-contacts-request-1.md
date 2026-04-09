
# V1 Contacts Request 1

## Structure

`V1ContactsRequest1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AccountNumber` | `string` | Optional | Contact Account Number<br><br>**Constraints**: *Maximum Length*: `32` |
| `ContactApiId` | `string` | Optional | Contact API Id<br><br>**Constraints**: *Maximum Length*: `64`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `FirstName` | `string` | Optional | First Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `LastName` | `string` | Optional | Last Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `CellPhone` | `string` | Optional | Cell phone of contact<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `Balance` | `double?` | Optional | Balance<br><br>**Constraints**: `>= -99999999.99`, `<= 99999999.99` |
| `Address` | [`Address`](../../doc/models/address.md) | Optional | Address of contact |
| `CompanyName` | `string` | Optional | Company Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `HeaderMessage` | `string` | Optional | Header Message<br><br>**Constraints**: *Maximum Length*: `250` |
| `DateOfBirth` | `string` | Optional | Contacts DOB, Format: yyyy-MM-dd<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `EmailTrxReceipt` | `bool?` | Optional | Whether or not to email all transactions receipts to contact (1 or 0) |
| `HomePhone` | `string` | Optional | Contacts home phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `OfficePhone` | `string` | Optional | Contacts office phone<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `OfficePhoneExt` | `string` | Optional | Contacts office phone extension for office phone<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^\d{1,10}$` |
| `HomePhoneCountryCode` | `string` | Optional | Home phone country code<br><br>**Constraints**: *Maximum Length*: `6`, *Pattern*: `^\+([\d]+)$` |
| `OfficePhoneCountryCode` | `string` | Optional | Office phone country code<br><br>**Constraints**: *Maximum Length*: `6`, *Pattern*: `^\+([\d]+)$` |
| `CellPhoneCountryCode` | `string` | Optional | Cell phone country code<br><br>**Constraints**: *Maximum Length*: `6`, *Pattern*: `^\+([\d]+)$` |
| `HeaderMessageType` | `int?` | Optional | Header Message Type<br><br>**Constraints**: `>= 0`, `<= 4` |
| `UpdateIfExists` | [`UpdateIfExistsEnum?`](../../doc/models/update-if-exists-enum.md) | Optional | Update If Exists |
| `ContactC1` | `string` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `ContactC2` | `string` | Optional | Custom field 2 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `ContactC3` | `string` | Optional | Custom field 3 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `ParentId` | `string` | Optional | Parent Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Email` | `string` | Optional | Email of contact<br><br>**Constraints**: *Maximum Length*: `64` |
| `TokenImportId` | `string` | Optional | Token Import Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_number": "54545433332",
  "contact_api_id": "137",
  "first_name": "John",
  "last_name": "Smith",
  "cell_phone": "3339998822",
  "balance": 245.36,
  "company_name": "Fortis Payment Systems, LLC",
  "header_message": "This is a sample message for you",
  "date_of_birth": "2021-12-01",
  "email_trx_receipt": true,
  "home_phone": "3339998822",
  "office_phone": "3339998822",
  "office_phone_ext": "5",
  "home_phone_country_code": "+1",
  "office_phone_country_code": "+1",
  "cell_phone_country_code": "+1",
  "header_message_type": 0,
  "update_if_exists": 1,
  "contact_c1": "any",
  "contact_c2": "anything",
  "contact_c3": "something",
  "parent_id": "11e95f8ec39de8fbdb0a4f1a",
  "email": "email@domain.com",
  "token_import_id": "11e95f8ec39de8fbdb0a4f1a"
}
```

