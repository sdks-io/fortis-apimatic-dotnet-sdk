
# Hosted Payment Page 1

*This model accepts additional fields of type object.*

## Structure

`HostedPaymentPage1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `UserId` | `string` | Optional | User ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `LocationApiId` | `string` | Optional | Location Api Id |
| `ProductTransactionId` | `string` | Optional | Product Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `RedirectUrlDelay` | `double?` | Optional | Redirect Url Delay<br><br>**Default**: `15`<br><br>**Constraints**: `<= 15` |
| `MinPaymentAmount` | `int?` | Optional | Min Payment Amount<br><br>**Constraints**: `>= 0` |
| `MaxPaymentAmount` | `long?` | Optional | Max Payment Amount<br><br>**Default**: `9999999999L`<br><br>**Constraints**: `<= 9999999999` |
| `RedirectUrlOnApprove` | `string` | Optional | Redirect Url On Approval |
| `RedirectUrlOnDecline` | `string` | Optional | Redirect Url On Decline |
| `FieldConfiguration` | [`FieldConfiguration2`](../../doc/models/field-configuration-2.md) | Optional | - |
| `EncryptionKey` | `string` | Optional | Encryption Key<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `32` |
| `StylesheetUrl` | `string` | Optional | Stylesheet Url |
| `ParentSendMessage` | `bool?` | Optional | Parent Send Message |
| `HideOptionalFields` | `bool?` | Optional | Hide Optional Fields |
| `Id` | `string` | Optional | Hosted Payment Page Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | System generated id for user who created record<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | System generated id for user who created record<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "title": "Sample title",
  "redirect_url_delay": 15,
  "min_payment_amount": 0,
  "max_payment_amount": 9999999999,
  "parent_send_message": true,
  "hide_optional_fields": true,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "location_api_id6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

