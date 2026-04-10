
# User

User

*This model accepts additional fields of type object.*

## Structure

`User`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Username` | `string` | Optional | Username |
| `FirstName` | `string` | Optional | First Name |
| `LastName` | `string` | Optional | Last Name |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "username": "email@domain.com",
  "first_name": "Bob",
  "last_name": "Fairview",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

