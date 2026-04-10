
# Filter By

*This model accepts additional fields of type object.*

## Structure

`FilterBy`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Key` | `string` | Required | Resource key to filter by |
| `Operator` | [`FilterByOperator`](../../doc/models/containers/filter-by-operator.md) | Required | This is a container for one-of cases. |
| `MValue` | [`FilterByValue`](../../doc/models/containers/filter-by-value.md) | Required | This is a container for one-of cases. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "key": "first_name",
  "operator": "<=",
  "value": "Fred",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

