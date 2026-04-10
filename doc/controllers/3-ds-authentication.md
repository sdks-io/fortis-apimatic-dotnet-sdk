# 3 DS Authentication

```csharp
M3DsAuthenticationController m3DsAuthenticationController = client.M3DsAuthenticationController;
```

## Class Name

`M3DsAuthenticationController`


# 3 DS Authentication Request

Makes a 3DS Authentication request to authenticate a card or begin the challenge flow.  If a challenge is required, a POST should be made to acs_url using the value of base64_encoded_challenge_request for the value of "creq" using x-www-form-urlencoded for the challenge request to the ACS.

```csharp
M3DsAuthenticationRequestAsync(
    Models.V1MerchantThreedsecureAuthenticationRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1MerchantThreedsecureAuthenticationRequest`](../../doc/models/v1-merchant-threedsecure-authentication-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseThreeDsAuthentication](../../doc/models/response-three-ds-authentication.md).

## Example Usage

```csharp
V1MerchantThreedsecureAuthenticationRequest body = new V1MerchantThreedsecureAuthenticationRequest
{
    ProductTransactionId = "11ee3860e2fc7f5ea67d36b3",
    DeviceChannel = DeviceChannel.Enum02,
    MessageCategory = MessageCategory.Enum82,
    ThreeDsRequestor = new ThreeDsRequestor1
    {
        ThreeDsRequestorAuthenticationInd = ThreeDsRequestorAuthenticationInd.Enum90,
        ThreeDsRequestorChallengeInd = new List<ThreeDsRequestorChallengeInd>
        {
            ThreeDsRequestorChallengeInd.Enum03,
        },
    },
    CardholderAccount = new CardholderAccount1
    {
        AccountNumber = "5454545454545454",
        SchemeId = SchemeId.Visa,
        ExpireDate = "2508",
    },
    EnforcePreferredProtocolVersion = true,
    ThreeDsCompInd = "Y",
};

try
{
    ApiResponse<ResponseThreeDsAuthentication> result = await m3DsAuthenticationController.M3DsAuthenticationRequestAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is V1MerchantThreedsecureAuthentication400ErrorException)
    {
       // TODO: Handle V1MerchantThreedsecureAuthentication400ErrorException exception here
    }
    if (e is Response401TokenException)
    {
       // TODO: Handle Response401TokenException exception here
    }
    if (e is Response412Exception)
    {
       // TODO: Handle Response412Exception exception here
    }
}
```

## Example Response *(as JSON)*

```json
{
  "type": "ThreeDSAuthentication",
  "data": {
    "three_ds_server_trans_id": "ea0c9973-4cd0-4f9f-83b3-609bf22c69e7",
    "acs_url": "https://api.sandbox.fortis.tech/v1/acs/challenge",
    "transaction_status": "C",
    "ds_trans_id": "278c7508-cac6-4233-902d-b90f31f741c6",
    "acs_trans_id": "d7c1ee99-9478-44a6-b1f2-391e29c6b340",
    "message_version": "2.2.0",
    "acs_challenge_mandated": "Y",
    "purchase_date": "20240509111532",
    "base64_encoded_challenge_request": "eyJtZXNzYWdlVHlwZSI6IkNSZXEiLCJ0aHJlZURTU2VydmVyVHJhbnNJRCI6ImVhMGM5OTczLTRjZDAtNGY5Zi04M2IzLTYwOWJmMjJjNjllNyIsImFjc1RyYW5zSUQiOiIwNWViNTE2OS02ZTFkLTQ5NTMtYWQ3NC1hZWU5YmQ4ZTc1YmIiLCJjaGFsbGVuZ2VXaW5kb3dTaXplIjoiMDEiLCJtZXNzYWdlVmVyc2lvbiI6IjIuMi4wIn0="
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Bad Request | [`V1MerchantThreedsecureAuthentication400ErrorException`](../../doc/models/v1-merchant-threedsecure-authentication-400-error-exception.md) |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

