
# Document

Array of document objects.

*This model accepts additional fields of type object.*

## Structure

`Document`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DocumentName` | `string` | Required | Array of bank account objects.<br><br>**Constraints**: *Maximum Length*: `32` |
| `DocumentData` | `string` | Required | Base64 encoded document content.<br><br>> Base64 encoded document content. |
| `MimeType` | `string` | Required | Mime type of document.<br><br>**Constraints**: *Maximum Length*: `20` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "document_name": "ImportantDoc.txt",
  "document_data": "alskj;asijia;eiom;weirj;iomj",
  "mime_type": "application/json",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

