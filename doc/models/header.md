
# Header

Header

*This model accepts additional fields of type object.*

## Structure

`Header`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Settings` | [`Settings`](../../doc/models/settings.md) | Optional | - |
| `Fields` | [`List<Field18>`](../../doc/models/field-18.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "settings": {
    "enabled": false,
    "columns": 202.28,
    "rows": 235.78,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "fields": [
    {
      "id": "id8",
      "label": "label8",
      "field_type": "field_type4",
      "position": [
        "position7",
        "position8",
        "position9"
      ],
      "required": false,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

