
# Address

Address of contact

## Structure

`Address`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `City` | `string` | Optional | City of contact<br><br>**Constraints**: *Maximum Length*: `36`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `State` | `string` | Optional | State of contact<br><br>**Constraints**: *Maximum Length*: `24` |
| `PostalCode` | `string` | Optional | Postal code of contact<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `Country` | `string` | Optional | The alpha 2 or alpha 3 format country code. If alpha 3 is provided, it will be converted to alpha 2. |
| `Street` | `string` | Optional | Street of contact<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |

## Example (as JSON)

```json
{
  "city": "Novi",
  "state": "Michigan",
  "postal_code": "48375",
  "country": "USA",
  "street": "street8"
}
```

