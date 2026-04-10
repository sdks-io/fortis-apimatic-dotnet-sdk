
# Three Ds Requestor Prior Authentication Info

*This model accepts additional fields of type object.*

## Structure

`ThreeDsRequestorPriorAuthenticationInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ThreeDsReqPriorRef` | `string` | Optional | This data element provides additional information to the ACS to determine the best approach for handling a request. The field is limited to 36 characters containing ACS Transaction ID for a prior authenticated transaction (for example, the first recurring transaction that was authenticated with the cardholder).<br><br>**Constraints**: *Maximum Length*: `36` |
| `ThreeDsReqPriorAuthMethod` | [`ThreeDsReqPriorAuthMethod?`](../../doc/models/three-ds-req-prior-auth-method.md) | Optional | **Constraints**: *Maximum Length*: `12` |
| `ThreeDsReqPriorAuthTimestamp` | `string` | Optional | Date and time converted into UTC of the prior authentication. Accepted date format is YYYYMMDDHHMM. |
| `ThreeDsReqPriorAuthData` | `string` | Optional | Data that documents and supports a specific authentication process. In the current version of the specification this data element is not defined in detail, however the intention is that for each 3DS Requestor Authentication Method, this field carry data that the ACS can use to verify the authentication process. In future versions of the application, these details are expected to be included.<br><br>**Constraints**: *Maximum Length*: `2048` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "three_ds_req_prior_ref": "three_ds_req_prior_ref8",
  "three_ds_req_prior_auth_method": "98",
  "three_ds_req_prior_auth_timestamp": "three_ds_req_prior_auth_timestamp8",
  "three_ds_req_prior_auth_data": "three_ds_req_prior_auth_data6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

