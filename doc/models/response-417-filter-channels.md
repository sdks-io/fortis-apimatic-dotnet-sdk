
# Response 417 Filter Channels

*This model accepts additional fields of type object.*

## Structure

`Response417FilterChannels`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatusCode` | `int?` | Optional | Response code |
| `Error` | `string` | Optional | Expectation Failed |
| `Message` | `string` | Optional | Channel filters are not set for this project |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "statusCode": 417,
  "error": "Expectation Failed",
  "message": "Channel filters are not set for this project",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

