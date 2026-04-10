
# Field

*This model accepts additional fields of type object.*

## Structure

`Field`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Field` | `string` | Optional | Field name used on the sort |
| `Order` | [`Order?`](../../doc/models/order.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "field": "last_name",
  "order": "asc",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

