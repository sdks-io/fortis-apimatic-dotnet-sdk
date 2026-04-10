
# Ui Prefs 1

*This model accepts additional fields of type object.*

## Structure

`UiPrefs1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EntryPage` | `string` | Optional | Ui Prefs Entry Page |
| `PageSize` | `int?` | Optional | Ui Prefs Page Size<br><br>**Constraints**: `>= 0`, `<= 99` |
| `ReportExportType` | `object` | Optional | - |
| `ProcessMethod` | `object` | Optional | - |
| `DefaultTerminal` | `string` | Optional | Ui Prefs Default Termianl<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "entry_page": "dashboard",
  "page_size": 2,
  "default_terminal": "11e95f8ec39de8fbdb0a4f1a",
  "report_export_type": {
    "key1": "val1",
    "key2": "val2"
  },
  "process_method": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

