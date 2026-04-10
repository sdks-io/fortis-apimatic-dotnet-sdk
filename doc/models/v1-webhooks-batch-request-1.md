
# V1 Webhooks Batch Request 1

*This model accepts additional fields of type object.*

## Structure

`V1WebhooksBatchRequest1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AttemptInterval` | `int?` | Optional | Number of seconds before another retry is submitted<br><br>**Default**: `300`<br><br>**Constraints**: `>= 300`, `<= 86400` |
| `BasicAuthUsername` | `string` | Optional | The Basic authorization username for the URL, if not supplied, the postback will be submitted without Basic authorization headers<br><br>> This is only expandable for response but settable in the POST/PUT request<br><br>**Constraints**: *Maximum Length*: `512` |
| `BasicAuthPassword` | `string` | Optional | The basic authorization password<br><br>> This is only expandable for response but settable in the POST/PUT request<br><br>**Constraints**: *Maximum Length*: `512` |
| `Expands` | `string` | Optional | An option list of expanded data to send with base data. (i.e. set this field to “contact,account_vault” to get the contact an accountvault used to run a transaction.)<br><br>**Constraints**: *Maximum Length*: `512` |
| `Format` | `object` | Optional | - |
| `IsActive` | `bool?` | Optional | Flag to indicate whether configuration is active (in effect). |
| `LocationId` | `string` | Optional | The location identifier of the resource you want to recieve postbacks from.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `LocationApiId` | `string` | Optional | Location Api ID |
| `OnCreate` | `bool?` | Optional | To receive postbacks on the creation of a resource |
| `OnUpdate` | `bool?` | Optional | To receive postbacks on the updating of a resource |
| `OnDelete` | `bool?` | Optional | To receive postbacks when the record is deleted |
| `Legacy` | `bool?` | Optional | Prefer the legacy api format.<br><br>**Default**: `true` |
| `PostbackConfigId` | `string` | Optional | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ProductTransactionId` | `string` | Optional | Required when using 'transaction' or 'transactionbatch' resource<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Resource` | `object` | Optional | - |
| `NumberOfAttempts` | `int?` | Optional | Maximum number of attempts on failure<br><br>**Constraints**: `>= 1`, `<= 5` |
| `Url` | `string` | Optional | The URL where the postback will be submitted<br><br>**Constraints**: *Maximum Length*: `512` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "attempt_interval": 300,
  "basic_auth_username": "tester",
  "basic_auth_password": "Test@522",
  "expands": "changelogs,tags",
  "is_active": true,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "on_create": true,
  "on_update": true,
  "on_delete": true,
  "legacy": true,
  "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "number_of_attempts": 1,
  "url": "https://127.0.0.1/receiver",
  "format": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

