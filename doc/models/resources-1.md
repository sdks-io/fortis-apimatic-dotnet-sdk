
# Resources 1

*This model accepts additional fields of type object.*

## Structure

`Resources1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Title` | `string` | Optional | Resource Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `Priv` | `string` | Optional | Priv<br><br>**Constraints**: *Maximum Length*: `64` |
| `ResourceName` | `string` | Optional | Resource Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `Id` | `int?` | Optional | Resource ID |
| `LastUsedDate` | `int?` | Optional | Last Used Date |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "title": "My terminal",
  "resource_name": "v2.addons.iframe.get",
  "id": 5693,
  "last_used_date": 1422040992,
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "priv": "priv0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

