
# Response 416 Date Range

*This model accepts additional fields of type object.*

## Structure

`Response416DateRange`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatusCode` | `int?` | Optional | Response code |
| `Error` | `string` | Optional | Requested Range Not Satisfiable |
| `Message` | `string` | Optional | The "fieldDate" should be less or equal to "ISODate". |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "statusCode": 416,
  "error": "Requested Range Not Satisfiable",
  "message": "The \"startDate\" should be less or equal \"2019-08-20T03:00:00.000Z\".",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

