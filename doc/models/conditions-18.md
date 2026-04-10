
# Conditions 18

*This model accepts additional fields of type object.*

## Structure

`Conditions18`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Method` | [`Method?`](../../doc/models/method.md) | Optional | - |
| `Values` | [`Values50?`](../../doc/models/values-50.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "xor",
  "values": "account_number",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

