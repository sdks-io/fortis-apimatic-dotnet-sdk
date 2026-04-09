
# Custom Header Signature



Documentation for accessing and setting credentials for user-api-key.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| UserApiKey | `string` | User API Key | `UserApiKey` | `UserApiKey` |



**Note:** Auth credentials can be set using `UserApiKeyCredentials` in the client builder and accessed through `UserApiKeyCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using FortisAPI.Standard;
using FortisAPI.Standard.Authentication;

namespace ConsoleApp;

FortisAPIClient client = new FortisAPIClient.Builder()
    .UserApiKeyCredentials(
        new UserApiKeyModel.Builder(
            "user-api-key"
        )
        .Build())
    .Build();
```


