
# Billing Address 5

Billing Address Object

*This model accepts additional fields of type object.*

## Structure

`BillingAddress5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PostalCode` | `string` | Optional | The Zip or 'Postal Code' portion of the address associated with the Credit Card.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `Street` | `string` | Optional | The Street portion of the address associated with the Credit Card.<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "postal_code": "48375",
  "street": "street4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

