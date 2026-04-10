
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
using FortisApi.Standard;
using FortisApi.Standard.Authentication;

namespace ConsoleApp;

FortisApiClient client = new FortisApiClient.Builder()
    .DeveloperIdCredentials(
        new DeveloperIdModel.Builder(
            "developer-id"
        )
        .Build())
    .Build();
```


