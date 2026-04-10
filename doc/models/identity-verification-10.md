
# Identity Verification 10

*This model accepts additional fields of type object.*

## Structure

`IdentityVerification10`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DlState` | `string` | Required | Required for ACH transactions when Driver's License Verification is enabled on the terminal.  Either dl_number + dl_state OR customer_id will need to be passed in this scenario.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `DlNumber` | `string` | Required | Required for ACH transactions when Driver's License Verification is enabled on the terminal.  Either dl_number + dl_state OR customer_id will need to be passed in this scenario.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `50` |
| `Ssn4` | `string` | Optional | For ACH transactions where Identity Verification is enabled for terminal. Only ssn4 or dob_year should be passed. not both.<br><br>**Constraints**: *Maximum Length*: `4` |
| `DobYear` | `string` | Optional | Required for certain ACH transactions where Identity Verification has been enabled for the terminal.  Either ssn4 or dob_year will need to be passed in this scenario but NOT BOTH.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `4`, *Pattern*: `^(19\d{2})\|20\d{2}$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "dl_state": "MI",
  "dl_number": "1235567",
  "ssn4": "8527",
  "dob_year": "1980",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

