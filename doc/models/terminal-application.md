
# Terminal Application

Terminal Application Information on `expand`

*This model accepts additional fields of type object.*

## Structure

`TerminalApplication`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Standalone` | `bool?` | Optional | Standalone |
| `EmvCapable` | `bool?` | Optional | Emv Capable |
| `NfcCapable` | `bool?` | Optional | Nfc Capable |
| `PinCapable` | `bool?` | Optional | Pin Capable |
| `PrintCapable` | `bool?` | Optional | Print Capable |
| `MsrCapable` | `bool?` | Optional | Msr Capable |
| `SigCaptureCapable` | `bool?` | Optional | Sig Capture Capable |
| `MposTerminal` | `bool?` | Optional | Mpos Terminal |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `48` |
| `Description` | `string` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `256` |
| `Id` | `string` | Optional | Terminal Application Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "standalone": true,
  "emv_capable": true,
  "nfc_capable": false,
  "pin_capable": true,
  "print_capable": false,
  "msr_capable": true,
  "sig_capture_capable": false,
  "mpos_terminal": false,
  "title": "Ingenico Link2500",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

