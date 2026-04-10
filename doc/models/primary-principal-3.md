
# Primary Principal 3

*This model accepts additional fields of type object.*

## Structure

`PrimaryPrincipal3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FirstName` | `string` | Optional | Signer's first name<br><br>**Constraints**: *Maximum Length*: `20` |
| `LastName` | `string` | Optional | Signer's last name<br><br>**Constraints**: *Maximum Length*: `20` |
| `MiddleName` | `string` | Optional | Signer's middle name<br><br>**Constraints**: *Maximum Length*: `20` |
| `Title` | `string` | Optional | Signer's title<br><br>**Constraints**: *Maximum Length*: `20` |
| `DateOfBirth` | `string` | Optional | Signer's date of birth<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `AddressLine1` | `string` | Optional | Signer's residential address line 1<br><br>**Constraints**: *Maximum Length*: `100` |
| `AddressLine2` | `string` | Optional | Signer's residential address line 2<br><br>**Constraints**: *Maximum Length*: `20` |
| `City` | `string` | Optional | Signer's city<br><br>**Constraints**: *Maximum Length*: `50` |
| `StateProvince` | `string` | Optional | Signer's two-digit state code<br><br>**Constraints**: *Maximum Length*: `2` |
| `PostalCode` | `string` | Optional | Signer's postal code<br><br>**Constraints**: *Maximum Length*: `10` |
| `Ssn` | `string` | Optional | Last four digits of the primary principal or Signer's social security number<br><br>**Constraints**: *Maximum Length*: `4` |
| `OwnershipPercent` | `int?` | Optional | Percentage of business owned by primary principal or signer<br><br>**Constraints**: `>= 0`, `<= 100` |
| `PhoneNumber` | `string` | Optional | Signer's phone number<br><br>**Constraints**: *Maximum Length*: `20` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
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
  "phone_number": "555-555-1234",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

