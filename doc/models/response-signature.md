
# Response Signature

*This model accepts additional fields of type object.*

## Structure

`ResponseSignature`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type72?`](../../doc/models/type-72.md) | Optional | - |
| `Data` | [`Data21`](../../doc/models/data-21.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Signature",
  "data": {
    "signature": "signature8",
    "resource": "AccountVault",
    "resource_id": "resource_id6",
    "id": "id0",
    "created_ts": 114,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

