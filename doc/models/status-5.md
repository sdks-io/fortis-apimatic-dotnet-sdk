
# Status 5

*This model accepts additional fields of type object.*

## Structure

`Status5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResponseCode` | `string` | Optional | Response code for API response.<br><br>**Constraints**: *Maximum Length*: `20` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "response_code": "Received",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

