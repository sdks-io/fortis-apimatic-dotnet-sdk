
# Order 21

*This model accepts additional fields of type object.*

## Structure

`Order21`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Key` | `string` | Required | Resource key to order by. |
| `Operator` | [`Operator`](../../doc/models/operator.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "key": "first_name",
  "operator": "asc",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

