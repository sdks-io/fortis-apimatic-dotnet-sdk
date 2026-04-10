
# Broad Info 1

*This model accepts additional fields of type object.*

## Structure

`BroadInfo1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Category` | [`Category?`](../../doc/models/category.md) | Optional | - |
| `Description` | `string` | Optional | Information to be broadcasted to the recipients. Accepted value length is maximum 4000 characters. This field is optional.<br><br>**Constraints**: *Maximum Length*: `4000` |
| `ExpireDate` | `string` | Optional | The date after which the relevance of the broadcasted information (e.g., ceritifacte expiration dates) expires. The accepted value length is 8 characters. The accepted format is YYYYMMDD.<br><br>**Constraints**: *Maximum Length*: `8` |
| `Severity` | [`Severity?`](../../doc/models/severity.md) | Optional | - |
| `Recipients` | [`Recipients?`](../../doc/models/recipients.md) | Optional | - |
| `Source` | [`Source?`](../../doc/models/source.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "category": "82",
  "description": "description6",
  "expire_date": "expire_date6",
  "severity": "03",
  "recipients": "01",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

