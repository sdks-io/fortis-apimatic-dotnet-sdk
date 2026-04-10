
# Data 13

*This model accepts additional fields of type object.*

## Structure

`Data13`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ThreeDsServerTransId` | `string` | Optional | Universally unique transaction identifier assigned by the 3DS Server to identify a single transaction. |
| `TransactionStatus` | `string` | Optional | Indicates whether a transaction qualifies as an authenticated transaction.  "D" and "I" are also applicable if the 3DS Server has initiated authentication with EMV 3DS 2.2.0 version or greater<br><br>> Y - Authentication / Account verification successful<br>> <br>> N - Not authenticated / Account not verified; Transaction denied<br>> <br>> U - Authentication / Account verification could not be performed; technical or other problem<br>> <br>> C - In order to complete the authentication, a challenge is required<br>> <br>> R - Authentication / Account verification Rejected. Issuer is rejecting authentication/verification and request that authorization not be attempted<br>> <br>> A - Attempts processing performed; Not authenticated / verified, but a proof of attempt authentication / verification is provided<br>> <br>> D - In order to complete the authentication, a challenge is required. Decoupled Authentication confirmed<br>> <br>> I - Informational Only; 3DS Requestor challenge preference acknowledged |
| `DsTransId` | `string` | Optional | Universally unique transaction identifier assigned by the DS to identify a single transaction. |
| `AcsTransId` | `string` | Optional | Universally unique transaction identifier assigned by the ACS to identify a single transaction. |
| `MessageVersion` | `string` | Optional | Protocol version identifier This shall be the Protocol Version Number of the specification utilised by the system creating this message.<br><br>The Message Version Number is set by the 3DS Server which originates the protocol with the AReq message. The Message Version Number does not change during a 3DS transaction. |
| `AuthenticationValue` | `string` | Optional | Payment System-specific value provided as part of the ACS registration for each supported DS. Authentication Value may be used to provide proof of authentication. |
| `Eci` | `string` | Optional | Payment System-specific value provided by the ACS to indicate the results of the attempt to authenticate the Cardholder. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "three_ds_server_trans_id": "516ef0bf-e510-4895-b0a8-c889f2eaf471",
  "transaction_status": "Y",
  "ds_trans_id": "f25084f0-5b16-4c0a-ae5d-b24808a95e4b",
  "acs_trans_id": "d7c1ee99-9478-44a6-b1f2-391e29c6b340",
  "message_version": "2.2.0",
  "authentication_value": "MTIzNDU2Nzg5MDA5ODc2NTQzMjE=",
  "eci": "05",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

