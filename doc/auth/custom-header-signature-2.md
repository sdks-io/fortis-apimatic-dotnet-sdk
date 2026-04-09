
# Custom Header Signature



Documentation for accessing and setting credentials for developer-id.

## Auth Credentials

| Name | Type | Description | Setter | Getter |
|  --- | --- | --- | --- | --- |
| DeveloperId | `string` | Developer ID | `DeveloperId` | `DeveloperId` |



**Note:** Auth credentials can be set using `DeveloperIdCredentials` in the client builder and accessed through `DeveloperIdCredentials` method in the client instance.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```csharp
using FortisAPI.Standard;
using FortisAPI.Standard.Authentication;

namespace ConsoleApp;

FortisAPIClient client = new FortisAPIClient.Builder()
    .DeveloperIdCredentials(
        new DeveloperIdModel.Builder(
            "developer-id"
        )
        .Build())
    .Build();
```


