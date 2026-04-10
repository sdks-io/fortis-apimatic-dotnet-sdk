
# V1 Transactions Void Request

*This model accepts additional fields of type object.*

## Structure

`V1TransactionsVoidRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tags` | `List<string>` | Optional | Tags |
| `Description` | `string` | Optional | Description<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "description": "some description",
  "tags": [
    "tags5",
    "tags6",
    "tags7"
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

