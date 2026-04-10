
# Custom Header Signature



Documentation for accessing and setting credentials for access-token.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| AccessToken | `string` | Access Token | `AccessToken` | `AccessToken` |



**Note:** Auth credentials can be set using `AccessTokenCredentials` in the client builder and accessed through `AccessTokenCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using FortisApi.Standard;
using FortisApi.Standard.Authentication;

namespace ConsoleApp;

FortisApiClient client = new FortisApiClient.Builder()
    .AccessTokenCredentials(
        new AccessTokenModel.Builder(
            "access-token"
        )
        .Build())
    .Build();
```


