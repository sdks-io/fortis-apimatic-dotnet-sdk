
# Item List 4

*This model accepts additional fields of type object.*

## Structure

`ItemList4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | Item's Name, must be unique on the list<br><br>**Constraints**: *Maximum Length*: `100` |
| `Amount` | `int` | Required | Item's Amount<br><br>**Constraints**: `>= -999999999`, `<= 999999999` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "name": "Bread",
  "amount": 2015,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

