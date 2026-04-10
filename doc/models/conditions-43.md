
# Conditions 43

*This model accepts additional fields of type object.*

## Structure

`Conditions43`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Method` | [`Method5?`](../../doc/models/method-5.md) | Optional | - |
| `Values` | [`Values7?`](../../doc/models/values-7.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "oxor",
  "values": "accountvault_c3",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

