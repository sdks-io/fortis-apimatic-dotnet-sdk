
# Address 4

*This model accepts additional fields of type object.*

## Structure

`Address4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `City` | `string` | Optional | City of contact<br><br>**Constraints**: *Maximum Length*: `36`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `State` | `string` | Optional | State of contact<br><br>**Constraints**: *Maximum Length*: `24` |
| `PostalCode` | `string` | Optional | Postal code of contact<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `Country` | `string` | Optional | The alpha 2 or alpha 3 format country code. If alpha 3 is provided, it will be converted to alpha 2. |
| `Street` | `string` | Optional | Street of contact<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "city": "Novi",
  "state": "Michigan",
  "postal_code": "48375",
  "country": "USA",
  "street": "street2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

