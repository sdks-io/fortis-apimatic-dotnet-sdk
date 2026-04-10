
# Field 18

*This model accepts additional fields of type object.*

## Structure

`Field18`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | id |
| `Label` | `string` | Optional | Label |
| `FieldType` | `string` | Optional | Field Type |
| `Position` | `List<string>` | Optional | Position<br><br>**Constraints**: *Minimum Items*: `1` |
| `Required` | `bool?` | Optional | Required |
| `Readonly` | `bool?` | Optional | Read Only |
| `Visible` | `bool?` | Optional | Visible |
| `MValue` | `string` | Optional | Value |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "transaction_amount",
  "label": "Header",
  "field_type": "heading",
  "position": [
    "1",
    "0",
    "1",
    "1"
  ],
  "required": true,
  "readonly": true,
  "visible": true,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

