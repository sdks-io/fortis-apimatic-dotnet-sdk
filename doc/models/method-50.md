
# Method 50

*This model accepts additional fields of type object.*

## Structure

`Method50`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type29`](../../doc/models/type-29.md) | Required | - |
| `ProductTransactionId` | `string` | Required | The product_transaction_id of the cc or ach deposit account that the transaction is inteded for. Use only the cc or ach id to display their respective elements form only. The Product's method (cc/ach) has to match the type.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ach",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

