
# Settings

*This model accepts additional fields of type object.*

## Structure

`Settings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Enabled` | `bool?` | Optional | Enabled |
| `Columns` | `double?` | Optional | Columns |
| `Rows` | `double?` | Optional | Rows |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "enabled": true,
  "columns": 1.0,
  "rows": 1.0,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

