
# Work Phone 2

*This model accepts additional fields of type object.*

## Structure

`WorkPhone2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cc` | `string` | Optional | Country Code of the phone<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `3` |
| `Subscriber` | `string` | Optional | Subscriber section of the number<br><br>**Constraints**: *Maximum Length*: `15` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "cc": "cc6",
  "subscriber": "subscriber8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

