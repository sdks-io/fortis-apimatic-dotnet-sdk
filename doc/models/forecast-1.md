
# Forecast 1

*This model accepts additional fields of type object.*

## Structure

`Forecast1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `RecurringId` | `string` | Optional | Recurring ID |
| `RecurringType` | `double?` | Optional | Recurring Type |
| `Amount` | `double?` | Optional | Amount |
| `Month` | `string` | Optional | Month |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_id": "Recurring ID",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "recurring_type": 113.38,
  "amount": 2.42,
  "month": "month0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

