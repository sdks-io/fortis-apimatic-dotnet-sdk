
# Contact 13

*This model accepts additional fields of type object.*

## Structure

`Contact13`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FirstName` | `string` | Optional | Contact's first name.<br><br>**Constraints**: *Maximum Length*: `20` |
| `LastName` | `string` | Optional | Contact's last name.<br><br>**Constraints**: *Maximum Length*: `20` |
| `Email` | `string` | Optional | Contact's email address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `PhoneNumber` | `string` | Required | Contact's phone.<br><br>**Constraints**: *Maximum Length*: `20` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "first_name": "Jeffery",
  "last_name": "Todd",
  "email": "jtodd@example.com",
  "phone_number": "555-555-3456",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

