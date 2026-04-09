
# Product Recurring

Product recurring array

## Structure

`ProductRecurring`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `LocationApiId` | `string` | Optional | Location Api ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `SendDeclinedNotifications` | `bool?` | Optional | Send Declined Notifications |
| `RequireFullPayment` | `bool?` | Optional | Require Full Payment |
| `ExpireNotificationEmailEnable` | `bool?` | Optional | Expire Notification Email Enable |
| `ExpireNotificationSmsEnable` | `bool?` | Optional | Expire Notification SMS Enable |
| `NotificationDaysDefault` | `int?` | Optional | Notification Days Default<br><br>**Constraints**: `>= 0`, `<= 365` |
| `Id` | `string` | Optional | Product Recurring Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | Created User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | Modified User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "title": "Fortispay RbYN6y",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "11e95f8ec39de8fbdb0a4f1a",
  "send_declined_notifications": true,
  "require_full_payment": true,
  "expire_notification_email_enable": true,
  "expire_notification_sms_enable": true,
  "notification_days_default": 1,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
}
```

