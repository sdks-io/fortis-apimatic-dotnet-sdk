
# Data 17

*This model accepts additional fields of type object.*

## Structure

`Data17`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Token` | `string` | Optional | JWT used to initialize the card reader |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "token": "token8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

