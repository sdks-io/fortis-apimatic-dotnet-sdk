
# Client Class Documentation

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| Environment | [`Environment`](../README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| Timeout | `TimeSpan` | Http client timeout.<br>*Default*: `TimeSpan.FromSeconds(100)` |
| HttpClientConfiguration | [`Action<HttpClientConfiguration.Builder>`](../doc/http-client-configuration-builder.md) | Action delegate that configures the HTTP client by using the HttpClientConfiguration.Builder for customizing API call settings.<br>*Default*: `new HttpClient()` |
| LogBuilder | [`LogBuilder`](../doc/log-builder.md) | Represents the logging configuration builder for API calls |
| UserIdCredentials | [`UserIdCredentials`](auth/custom-header-signature.md) | The Credentials Setter for Custom Header Signature |
| UserApiKeyCredentials | [`UserApiKeyCredentials`](auth/custom-header-signature-1.md) | The Credentials Setter for Custom Header Signature |
| DeveloperIdCredentials | [`DeveloperIdCredentials`](auth/custom-header-signature-2.md) | The Credentials Setter for Custom Header Signature |
| AccessTokenCredentials | [`AccessTokenCredentials`](auth/custom-header-signature-3.md) | The Credentials Setter for Custom Header Signature |

The API client can be initialized as follows:

## Code-Based Initialization

```csharp
using FortisApi.Standard;
using FortisApi.Standard.Authentication;
using Microsoft.Extensions.Logging;

namespace ConsoleApp;

FortisApiClient client = new FortisApiClient.Builder()
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
    .Environment(FortisApi.Standard.Environment.Production)
    .LoggingConfig(config => config
        .LogLevel(LogLevel.Information)
        .RequestConfig(reqConfig => reqConfig.Body(true))
        .ResponseConfig(respConfig => respConfig.Headers(true))
    )
    .Build();
```

## Configuration-Based Initialization

```csharp
using FortisApi.Standard;
using Microsoft.Extensions.Configuration;

namespace ConsoleApp;

// Build the IConfiguration using .NET conventions (JSON, environment, etc.)
var configuration = new ConfigurationBuilder()
    .AddJsonFile("config.json")
    .AddEnvironmentVariables() // [optional] read environment variables
    .Build();

// Instantiate your SDK and configure it from IConfiguration
var client = FortisApiClient
    .FromConfiguration(configuration.GetSection("FortisApi"));
```

See the [Configuration-Based Initialization](../doc/configuration-based-initialization.md) section for details.

## Fortis APIClient Class

The gateway for the SDK. This class acts as a factory for the Controllers and also holds the configuration of the SDK.

### Controllers

| Name | Description |
|  --- | --- |
| AsyncProcessingController | Gets AsyncProcessingController controller. |
| BatchesController | Gets BatchesController controller. |
| ContactsController | Gets ContactsController controller. |
| DeclinedRecurringTransactionsController | Gets DeclinedRecurringTransactionsController controller. |
| DeviceTermsController | Gets DeviceTermsController controller. |
| ElementsController | Gets ElementsController controller. |
| FullBoardingController | Gets FullBoardingController controller. |
| LocationsController | Gets LocationsController controller. |
| M3DsAuthenticationController | Gets M3DsAuthenticationController controller. |
| M3DsTransactionsController | Gets M3DsTransactionsController controller. |
| MerchantDepositsController | Gets MerchantDepositsController controller. |
| OnBoardingController | Gets OnBoardingController controller. |
| PaylinksController | Gets PaylinksController controller. |
| PaymentCardReaderTokenController | Gets PaymentCardReaderTokenController controller. |
| QuickInvoicesController | Gets QuickInvoicesController controller. |
| RecurringController | Gets RecurringController controller. |
| SignaturesController | Gets SignaturesController controller. |
| TagsController | Gets TagsController controller. |
| TerminalsController | Gets TerminalsController controller. |
| TicketsController | Gets TicketsController controller. |
| TokensController | Gets TokensController controller. |
| TransactionAchRetriesController | Gets TransactionAchRetriesController controller. |
| TransactionsAchController | Gets TransactionsAchController controller. |
| TransactionsCashController | Gets TransactionsCashController controller. |
| TransactionsCreditCardController | Gets TransactionsCreditCardController controller. |
| TransactionsEbtCardController | Gets TransactionsEbtCardController controller. |
| TransactionsReadController | Gets TransactionsReadController controller. |
| Level3DataController | Gets Level3DataController controller. |
| TransactionsUpdatesController | Gets TransactionsUpdatesController controller. |
| UserVerificationsController | Gets UserVerificationsController controller. |
| UsersController | Gets UsersController controller. |
| ApplePayValidateMerchantController | Gets ApplePayValidateMerchantController controller. |
| MerchantDetailsController | Gets MerchantDetailsController controller. |
| WebhooksController | Gets WebhooksController controller. |

### Properties

| Name | Description | Type |
|  --- | --- | --- |
| HttpClientConfiguration | Gets the configuration of the Http Client associated with this client. | [`IHttpClientConfiguration`](../doc/http-client-configuration.md) |
| Timeout | Http client timeout. | `TimeSpan` |
| Environment | Current API environment. | `Environment` |
| UserIdCredentials | Gets the credentials to use with UserId. | [`IUserIdCredentials`](auth/custom-header-signature.md) |
| UserApiKeyCredentials | Gets the credentials to use with UserApiKey. | [`IUserApiKeyCredentials`](auth/custom-header-signature-1.md) |
| DeveloperIdCredentials | Gets the credentials to use with DeveloperId. | [`IDeveloperIdCredentials`](auth/custom-header-signature-2.md) |
| AccessTokenCredentials | Gets the credentials to use with AccessToken. | [`IAccessTokenCredentials`](auth/custom-header-signature-3.md) |

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `GetBaseUri(Server alias = Server.Default)` | Gets the URL for a particular alias in the current environment and appends it with template parameters. | `string` |
| `ToBuilder()` | Creates an object of the Fortis APIClient using the values provided for the builder. | `Builder` |

## Fortis APIClient Builder Class

Class to build instances of Fortis APIClient.

### Methods

| Name | Description | Return Type |
|  --- | --- | --- |
| `HttpClientConfiguration(Action<`[`HttpClientConfiguration.Builder`](../doc/http-client-configuration-builder.md)`> action)` | Gets the configuration of the Http Client associated with this client. | `Builder` |
| `Timeout(TimeSpan timeout)` | Http client timeout. | `Builder` |
| `Environment(Environment environment)` | Current API environment. | `Builder` |
| `UserIdCredentials(Action<UserIdModel.Builder> action)` | Sets credentials for UserId. | `Builder` |
| `UserApiKeyCredentials(Action<UserApiKeyModel.Builder> action)` | Sets credentials for UserApiKey. | `Builder` |
| `DeveloperIdCredentials(Action<DeveloperIdModel.Builder> action)` | Sets credentials for DeveloperId. | `Builder` |
| `AccessTokenCredentials(Action<AccessTokenModel.Builder> action)` | Sets credentials for AccessToken. | `Builder` |

