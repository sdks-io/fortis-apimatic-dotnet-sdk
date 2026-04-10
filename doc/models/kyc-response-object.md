
# Kyc Response Object

Array of KYC response objects.

*This model accepts additional fields of type object.*

## Structure

`KycResponseObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `MValue` | `string` | Required | KYC object value. |
| `Type` | `string` | Required | KYC oject type.<br><br>**Constraints**: *Maximum Length*: `32` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "value": "KYC value.",
  "type": "KYC type",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

