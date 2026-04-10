
# V1 Tokens Cc Request 1

*This model accepts additional fields of type object.*

## Structure

`V1TokensCcRequest1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AccountHolderName` | `string` | Optional | Account holder name<br><br>> For CC, this is the 'Name (as it appears) on Card'. For ACH, this is the 'Name on Account'.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `32` |
| `AccountVaultApiId` | `string` | Optional | This field can be used to correlate Tokens in our system to data within an outside software integration<br><br>> Must be unique per location. When running a transaction and using a stored token, this field can be used in place of account_vault_id.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `TokenApiId` | `string` | Optional | This field can be used to correlate Tokens in our system to data within an outside software integration<br><br>> Must be unique per location. When running a transaction and using a stored token, this field can be used in place of token_id.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `AccountvaultC1` | `string` | Optional | DEPRECATED (Use token_c1 instead)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AccountvaultC2` | `string` | Optional | DEPRECATED (Use token_c2 instead)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AccountvaultC3` | `string` | Optional | DEPRECATED (Use token_c3 instead)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `TokenC1` | `string` | Optional | Custom field 1 for API users to store custom data<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `TokenC2` | `string` | Optional | Custom field 2 for API users to store custom data<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `TokenC3` | `string` | Optional | Custom field 3 for API users to store custom data<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AchSecCode` | `object` | Optional | - |
| `BillingAddress` | [`BillingAddress7`](../../doc/models/billing-address-7.md) | Optional | - |
| `ContactId` | `string` | Optional | Used to associate the Token with a Contact.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CustomerId` | `string` | Optional | Used to store a customer identification number.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `50` |
| `IdentityVerification` | [`IdentityVerification5`](../../doc/models/identity-verification-5.md) | Optional | - |
| `LocationId` | `string` | Optional | A valid Location Id associated with the Contact for this Token<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `PreviousAccountVaultApiId` | `string` | Optional | Can be used to pull payment info from a previous token api id.<br><br>**Constraints**: *Maximum Length*: `64` |
| `PreviousTokenApiId` | `string` | Optional | Can be used to pull payment info from a previous token api id.<br><br>**Constraints**: *Maximum Length*: `64` |
| `PreviousAccountVaultId` | `string` | Optional | Can be used to pull payment info from a previous token.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `PreviousTokenId` | `string` | Optional | Can be used to pull payment info from a previous token.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `PreviousTransactionId` | `string` | Optional | Can be used to pull payment info from a previous transaction.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AccountNumber` | `string` | Optional | Account number<br><br>> For CC transactions, a credit card number. For ACH transactions, a bank account number. String lengths are conditional, CC should be 13-19 and ACH should be 4-19.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `19`, *Pattern*: `^[\d]+$` |
| `TermsAgree` | `bool?` | Optional | Terms agreement. |
| `TermsAgreeIp` | `string` | Optional | The ip address of the client that agreed to terms. |
| `Title` | `string` | Optional | Used to describe the Token for easier identification within our UI.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `16` |
| `TokenImportId` | `string` | Optional | Token Import Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `SecureDirectoryServerTransactionId` | `string` | Optional | (ECOMM) Directory Server Transaction ID (Such as XID, TAVV) |
| `SecureProtocolVersion` | `int?` | Optional | (ECOMM)  Secure Program Protocol Version |
| `SecureAuthData` | `string` | Optional | (ECOMM) The token authentication value associated with 3D secure transactions (Such as CAVV, UCAF auth data) |
| `SecureCollectionIndicator` | `int?` | Optional | (ECOMM) Used for UCAF collection indicator or Discover Autentication type |
| `ThreeDsServerTransId` | `string` | Optional | 3DS Server Transaction ID.  If this field is sent and 3DS authentication was done with Fortis, the 3DS fields secure_directory_server_transaction_id, secure_protocol_version, and secure_collection_indicator will be pre-populated. |
| `AcsTransactionId` | `string` | Optional | ACS Transaction ID<br><br>**Constraints**: *Maximum Length*: `36` |
| `Joi` | [`Joi4`](../../doc/models/joi-4.md) | Optional | - |
| `ExpDate` | `string` | Optional | Required for CC. The Expiration Date for the credit card. (MMYY format).<br><br>**Constraints**: *Pattern*: `^(0[1-9]\|1[0-2])[0-9]{2}$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "account_holder_name": "John Smith",
  "account_vault_api_id": "accountvaultabcd",
  "token_api_id": "tokenabcd",
  "accountvault_c1": "accountvault custom 1",
  "accountvault_c2": "accountvault custom 2",
  "accountvault_c3": "accountvault custom 3",
  "token_c1": "token custom 1",
  "token_c2": "token custom 2",
  "token_c3": "token custom 3",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "customer_id": "123456",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "previous_account_vault_api_id": "previousaccountvault123456",
  "previous_token_api_id": "previousaccountvault123456",
  "previous_account_vault_id": "11e95f8ec39de8fbdb0a4f1a",
  "previous_token_id": "11e95f8ec39de8fbdb0a4f1a",
  "previous_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_number": "545454545454545",
  "terms_agree": true,
  "terms_agree_ip": "192.168.0.10",
  "title": "Test CC Account",
  "token_import_id": "11e95f8ec39de8fbdb0a4f1a",
  "secure_directory_server_transaction_id": "d65e93c3-35ab-41ba-b307-767bfc19eae",
  "secure_protocol_version": 2,
  "secure_auth_data": "vVwL7UNHCf8W8M2LAfvRChNHN7c%3D",
  "three_ds_server_trans_id": "d65e93c3-35ab-41ba-b307-767bfc19eae",
  "acs_transaction_id": "13c701a3-5a88-4c45-89e9-ef65e50a8bf9",
  "exp_date": "0929",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

