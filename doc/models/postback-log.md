
# Postback Log

*This model accepts additional fields of type object.*

## Structure

`PostbackLog`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PostbackStatusId` | `object` | Optional | - |
| `Id` | `string` | Optional | Postback Log Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `PostbackConfigId` | `string` | Optional | Postback Config Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ChangelogId` | `string` | Optional | Changelog Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `HttpVerb` | `string` | Optional | Http Verb |
| `NextRunTs` | `int?` | Optional | Next Run |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `Model` | `string` | Optional | MOdel |
| `ModelId` | `string` | Optional | Model Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
  "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
  "next_run_ts": 1422040992,
  "created_ts": 1422040992,
  "model_id": "11e95f8ec39de8fbdb0a4f1a",
  "postback_status_id": {
    "key1": "val1",
    "key2": "val2"
  },
  "http_verb": "http_verb8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

