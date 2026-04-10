
# File

*This model accepts additional fields of type object.*

## Structure

`File`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `File` | `object` | Optional | File Object |
| `ResourceId` | `string` | Optional | Resource Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Resource` | [`Resource2?`](../../doc/models/resource-2.md) | Optional | - |
| `ProductFileId` | `string` | Optional | Product File Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `FileCategoryId` | `string` | Optional | File Category Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `VisibilityGroupId` | `string` | Optional | Visibility Group Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `FileDescription` | `string` | Optional | File Description<br><br>**Constraints**: *Maximum Length*: `128` |
| `Id` | `string` | Optional | Resource<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `FileName` | `string` | Optional | File Name |
| `FileExtension` | `string` | Optional | File Extension<br><br>**Constraints**: *Maximum Length*: `4` |
| `FileSizeBytes` | `int?` | Optional | File Size Bytes |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "resource_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_file_id": "11e95f8ec39de8fbdb0a4f1a",
  "file_category_id": "11e95f8ec39de8fbdb0a4f1a",
  "visibility_group_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "file": {
    "key1": "val1",
    "key2": "val2"
  },
  "resource": "Location",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

