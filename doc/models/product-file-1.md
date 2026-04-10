
# Product File 1

*This model accepts additional fields of type object.*

## Structure

`ProductFile1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `ProductFileCredentialId` | `string` | Optional | Product File Credential Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `FreeBytes` | `double?` | Optional | Free Bytes |
| `ByteIncrement` | `double?` | Optional | Byte Increment |
| `MaxFileSizeBytes` | `double?` | Optional | Max File Size Bytes |
| `IncrementCost` | `double?` | Optional | Increment Cost |
| `MonthlyFee` | `int?` | Optional | Monthly Fee |
| `FileExtAllowed` | `string` | Optional | File Ext Allowed<br><br>**Constraints**: *Maximum Length*: `64` |
| `Container` | `string` | Optional | Container<br><br>**Constraints**: *Maximum Length*: `128` |
| `Id` | `string` | Optional | Product File Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `Active` | `bool?` | Optional | Active |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "title": "My terminal",
  "product_file_credential_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "active": true,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "free_bytes": 13.42,
  "byte_increment": 16.74,
  "max_file_size_bytes": 221.86,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

