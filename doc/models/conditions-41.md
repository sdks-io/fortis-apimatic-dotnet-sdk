
# Conditions 41

*This model accepts additional fields of type object.*

## Structure

`Conditions41`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Method` | [`Method5?`](../../doc/models/method-5.md) | Optional | - |
| `Values` | [`Values5?`](../../doc/models/values-5.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "oxor",
  "values": "accountvault_c1",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

