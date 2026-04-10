
# Received Email

*This model accepts additional fields of type object.*

## Structure

`ReceivedEmail`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Subject` | `string` | Optional | Subject<br><br>**Constraints**: *Maximum Length*: `256` |
| `Body` | `string` | Optional | Body |
| `SourceAddress` | `string` | Optional | Source Address<br><br>**Constraints**: *Maximum Length*: `64` |
| `ReturnPath` | `string` | Optional | Return Path<br><br>**Constraints**: *Maximum Length*: `64` |
| `ProviderId` | `string` | Optional | Provider<br><br>**Constraints**: *Maximum Length*: `60` |
| `DomainId` | `string` | Optional | Domain<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ReasonSent` | `string` | Optional | Reason Sent<br><br>**Constraints**: *Maximum Length*: `36` |
| `ReasonModel` | `object` | Optional | - |
| `ReasonModelId` | `string` | Optional | Reason Model<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ReplyTo` | `string` | Optional | Reply To<br><br>**Constraints**: *Maximum Length*: `520` |
| `Id` | `string` | Optional | Log Email Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "subject": "Payment Receipt - 12skiestech",
  "body": "This email is being sent from a server.",
  "source_address": "\"12skiestech A7t3qi\" <noreply@zeamster.email>",
  "return_path": "\"12skiestech A7t3qi\" <noreply@zeamster.email>",
  "provider_id": "0100017e67bcc530-e1dd23b4-8a39-4a5b-8d5d-68d51c4c942f-000000",
  "domain_id": "11e95f8ec39de8fbdb0a4f1a",
  "reason_sent": "Contact Email",
  "reason_model_id": "11e95f8ec39de8fbdb0a4f1a",
  "reply_to": "\"Zeamster\" <emma.p@zeamster.com>",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

