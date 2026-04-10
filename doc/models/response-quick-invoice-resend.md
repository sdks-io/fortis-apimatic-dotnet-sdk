
# Response Quick Invoice Resend

*This model accepts additional fields of type object.*

## Structure

`ResponseQuickInvoiceResend`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`Type61?`](../../doc/models/type-61.md) | Optional | - |
| `Data` | [`Data19`](../../doc/models/data-19.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "QuickInvoiceResend",
  "data": {
    "id": "id0",
    "email_log_id": "email_log_id2",
    "sms_log_id": "sms_log_id4",
    "success": false,
    "sms_success": false,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

