
# Address 3

*This model accepts additional fields of type object.*

## Structure

`Address3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `City` | `string` | Optional | City name<br><br>**Constraints**: *Maximum Length*: `36`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `State` | `string` | Optional | State name<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `PostalCode` | `string` | Optional | Postal code<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `Country` | `object` | Optional | - |
| `Street` | `string` | Optional | Street<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "city": "Novi",
  "state": "MI",
  "postal_code": "48375",
  "country": {
    "key1": "val1",
    "key2": "val2"
  },
  "street": "street0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

