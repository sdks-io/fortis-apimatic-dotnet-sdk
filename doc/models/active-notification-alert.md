
# Active Notification Alert

*This model accepts additional fields of type object.*

## Structure

`ActiveNotificationAlert`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `LocationApiId` | `string` | Optional | Location Api ID |
| `DateStart` | `string` | Optional | Date Start<br><br>**Constraints**: *Maximum Length*: `19`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}\s[\d]{2}:[\d]{2}:[\d]{2}$` |
| `DateEnd` | `string` | Optional | Date End<br><br>**Constraints**: *Maximum Length*: `19`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}\s[\d]{2}:[\d]{2}:[\d]{2}$` |
| `UserLocation` | `bool?` | Optional | User Location |
| `UserContact` | `bool?` | Optional | User Contact |
| `IncludeChildren` | `bool?` | Optional | Include Children |
| `AlertType` | `object` | Optional | - |
| `AlertTypeId` | `object` | Optional | - |
| `Description` | `string` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `32` |
| `AlertMessage` | `string` | Optional | Alert Message |
| `Id` | `string` | Optional | Notification Alert ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "date_start": "2021-12-01 10:10:00",
  "date_end": "2021-12-01 10:10:00",
  "user_location": true,
  "user_contact": true,
  "include_children": true,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "location_api_id4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

