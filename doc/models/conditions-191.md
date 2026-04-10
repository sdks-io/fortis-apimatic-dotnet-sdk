
# Conditions 191

*This model accepts additional fields of type object.*

## Structure

`Conditions191`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Method` | [`Method53?`](../../doc/models/method-53.md) | Optional | - |
| `Values` | [`Values58?`](../../doc/models/values-58.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "and",
  "values": "account_number",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

