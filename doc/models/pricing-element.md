
# Pricing Element

Array of pricing items from template to be changed.

*This model accepts additional fields of type object.*

## Structure

`PricingElement`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ItemId` | `int` | Required | Item ID.<br><br>**Constraints**: `>= 0` |
| `ItemValue` | `double` | Required | Item value.<br><br>**Constraints**: `>= 0` |
| `ItemTerm` | `int` | Required | Item term.<br><br>**Constraints**: `>= 0` |
| `ItemDescription` | `string` | Optional | Item desciption.<br><br>**Constraints**: *Maximum Length*: `100` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "item_id": 5,
  "item_value": 1.5,
  "item_term": 2,
  "item_description": "AVS fee.",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

