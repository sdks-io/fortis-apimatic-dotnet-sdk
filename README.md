
# Getting Started with Fortis API

## Install the Package

If you are building with .NET CLI tools then you can also use the following command:

```bash
dotnet add package FortisApimaticSDK --version 1.0.0
```

You can also view the package at:
https://www.nuget.org/packages/FortisApimaticSDK/1.0.0

## Test the SDK

The generated SDK also contain one or more Tests, which are contained in the Tests project. In order to invoke these test cases, you will need `NUnit 3.0 Test Adapter Extension` for Visual Studio. Once the SDK is complied, the test cases should appear in the Test Explorer window. Here, you can click `Run All` to execute these test cases.

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Environment | [`Environment`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/README.md#environments) | The API environment. <br> **Default: `Environment.Sandbox`** |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(100)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-client-configuration-builder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| UserIdCredentials | [`UserIdCredentials`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| UserApiKeyCredentials | [`UserApiKeyCredentials`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature-1.md) | The Credentials Setter for Custom Header Signature |
| DeveloperIdCredentials | [`DeveloperIdCredentials`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature-2.md) | The Credentials Setter for Custom Header Signature |
| AccessTokenCredentials | [`AccessTokenCredentials`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature-3.md) | The Credentials Setter for Custom Header Signature |

The API client can be initialized as follows:

### Code-Based Initialization

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
    .UserApiKeyCredentials(
        new UserApiKeyModel.Builder(
            "user-api-key"
        )
        .Build())
    .DeveloperIdCredentials(
        new DeveloperIdModel.Builder(
            "developer-id"
        )
        .Build())
    .AccessTokenCredentials(
        new AccessTokenModel.Builder(
            "access-token"
        )
        .Build())
    .HttpClientConfig(httpClientConfig =>
        httpClientConfig.Timeout(TimeSpan.FromSeconds(100)))
    .Environment(FortisAPI.Standard.Environment.Sandbox)
    .Build();
```

### Configuration-Based Initialization

```csharp
using FortisAPI.Standard;
using Microsoft.Extensions.Configuration;

namespace ConsoleApp;

// Build the IConfiguration using .NET conventions (JSON, environment, etc.)
var configuration = new ConfigurationBuilder()
    .AddJsonFile("config.json")
    .AddEnvironmentVariables() // [optional] read environment variables
    .Build();

// Instantiate your SDK and configure it from IConfiguration
var client = FortisAPIClient
    .FromConfiguration(configuration.GetSection("FortisAPI"));
```

See the [Configuration-Based Initialization](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/configuration-based-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| Sandbox | **Default** |
| Production | - |

## Authorization

This API uses the following authentication schemes.

* [`user-id (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature.md)
* [`user-api-key (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature-1.md)
* [`developer-id (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature-2.md)
* [`access-token (Custom Header Signature)`](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/auth/custom-header-signature-3.md)

## List of APIs

* [Async Processing](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/async-processing.md)
* [Declined Recurring Transactions](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/declined-recurring-transactions.md)
* [Device Terms](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/device-terms.md)
* [Full Boarding](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/full-boarding.md)
* [3 DS Authentication](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/3-ds-authentication.md)
* [3 DS Transactions](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/3-ds-transactions.md)
* [Merchant Deposits](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/merchant-deposits.md)
* [On Boarding](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/on-boarding.md)
* [Payment Card Reader Token](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/payment-card-reader-token.md)
* [Quick Invoices](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/quick-invoices.md)
* [Transaction ACH Retries](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transaction-ach-retries.md)
* [Transactions-ACH](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transactions-ach.md)
* [Transactions-Cash](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transactions-cash.md)
* [Transactions-Credit Card](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transactions-credit-card.md)
* [Transactions-EBT Card](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transactions-ebt-card.md)
* [Transactions-Read](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transactions-read.md)
* [Level 3 Data](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/level-3-data.md)
* [Transactions-Updates](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/transactions-updates.md)
* [User Verifications](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/user-verifications.md)
* [Apple Pay Validate Merchant](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/apple-pay-validate-merchant.md)
* [Merchant Details](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/merchant-details.md)
* [Batches](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/batches.md)
* [Contacts](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/contacts.md)
* [Elements](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/elements.md)
* [Locations](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/locations.md)
* [Paylinks](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/paylinks.md)
* [Recurring](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/recurring.md)
* [Signatures](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/signatures.md)
* [Tags](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/tags.md)
* [Terminals](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/terminals.md)
* [Tickets](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/tickets.md)
* [Tokens](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/tokens.md)
* [Users](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/users.md)
* [Webhooks](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/controllers/webhooks.md)

## SDK Infrastructure

### Configuration

* [Configuration-Based Initialization](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/configuration-based-initialization.md)
* [HttpClientConfiguration](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-client-configuration.md)
* [HttpClientConfigurationBuilder](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-client-configuration-builder.md)
* [ProxyConfigurationBuilder](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/proxy-configuration-builder.md)

### HTTP

* [HttpCallback](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-callback.md)
* [HttpContext](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-context.md)
* [HttpRequest](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-request.md)
* [HttpResponse](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-response.md)
* [HttpStringResponse](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/http-string-response.md)

### Utilities

* [ApiException](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/api-exception.md)
* [ApiHelper](https://www.github.com/sdks-io/fortis-apimatic-dotnet-sdk/tree/1.0.0/doc/api-helper.md)

