
# Sort

Sort information used on the results

## Structure

`Sort`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type4Enum?`](../../doc/models/type-4-enum.md) | Optional | Object type |
| `Fields` | [`List<Field>`](../../doc/models/field.md) | Optional | [object Object] |

## Example (as JSON)

```json
{
  "type": "Sorting",
  "fields": [
    {
      "field": "field2",
      "order": "asc"
    },
    {
      "field": "field2",
      "order": "asc"
    }
  ]
}
```

