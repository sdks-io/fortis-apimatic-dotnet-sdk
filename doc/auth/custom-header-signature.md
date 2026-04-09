
# Custom Header Signature



Documentation for accessing and setting credentials for user-id.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| UserId | `string` | User ID | `UserId` | `UserId` |



**Note:** Auth credentials can be set using `UserIdCredentials` in the client builder and accessed through `UserIdCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using FortisAPI.Standard;
using FortisAPI.Standard.Authentication;

namespace ConsoleApp;

FortisAPIClient client = new FortisAPIClient.Builder()
    .UserIdCredentials(
        new UserIdModel.Builder(
            "user-id"
        )
        .Build())
    .Build();
```


