
# Data 19

## Structure

`Data19`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | Quick Invoice ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `EmailLogId` | `string` | Optional | Email Log Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `SmsLogId` | `string` | Optional | SMS Log Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Success` | `bool?` | Optional | Success |
| `SmsSuccess` | `bool?` | Optional | SMS Success |
| `Email` | `string` | Optional | Email<br><br>**Constraints**: *Maximum Length*: `64` |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "email_log_id": "11e95f8ec39de8fbdb0a4f1a",
  "sms_log_id": "11e95f8ec39de8fbdb0a4f1a",
  "success": true,
  "sms_success": true,
  "email": "email@domain.com"
}
```

