# Webhooks

```csharp
WebhooksController webhooksController = client.WebhooksController;
```

## Class Name

`WebhooksController`

## Methods

* [Createanewtransactionbatchpostbackconfig](../../doc/controllers/webhooks.md#createanewtransactionbatchpostbackconfig)
* [Createanewcontactpostbackconfig](../../doc/controllers/webhooks.md#createanewcontactpostbackconfig)
* [Createanewtransactionpostbackconfig](../../doc/controllers/webhooks.md#createanewtransactionpostbackconfig)
* [Deleteapostbackconfig](../../doc/controllers/webhooks.md#deleteapostbackconfig)
* [Updatetransactionbatchpostbackconfig](../../doc/controllers/webhooks.md#updatetransactionbatchpostbackconfig)
* [Updatecontactpostbackconfig](../../doc/controllers/webhooks.md#updatecontactpostbackconfig)
* [Updatetransactionpostbackconfig](../../doc/controllers/webhooks.md#updatetransactionpostbackconfig)


# Createanewtransactionbatchpostbackconfig

```csharp
CreateanewtransactionbatchpostbackconfigAsync(
    Models.V1WebhooksBatchRequest body,
    List<Models.Expand123> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WebhooksBatchRequest`](../../doc/models/v1-webhooks-batch-request.md) | Body, Required | - |
| `expand` | [`List<Expand123>`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
V1WebhooksBatchRequest body = new V1WebhooksBatchRequest
{
    IsActive = true,
    LocationId = "11e95f8ec39de8fbdb0a4f1a",
    OnCreate = true,
    OnUpdate = true,
    OnDelete = true,
    ProductTransactionId = "11e95f8ec39de8fbdb0a4f1a",
    NumberOfAttempts = 1,
    Url = "https://127.0.0.1/receiver",
    AttemptInterval = 300,
    BasicAuthUsername = "tester",
    BasicAuthPassword = "Test@522",
    Expands = "changelogs,tags",
    Legacy = true,
    PostbackConfigId = "11e95f8ec39de8fbdb0a4f1a",
};

try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.CreateanewtransactionbatchpostbackconfigAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Createanewcontactpostbackconfig

```csharp
CreateanewcontactpostbackconfigAsync(
    Models.V1WebhooksContactRequest body,
    List<Models.Expand123> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WebhooksContactRequest`](../../doc/models/v1-webhooks-contact-request.md) | Body, Required | - |
| `expand` | [`List<Expand123>`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
V1WebhooksContactRequest body = new V1WebhooksContactRequest
{
    IsActive = true,
    LocationId = "11e95f8ec39de8fbdb0a4f1a",
    OnCreate = true,
    OnUpdate = true,
    OnDelete = true,
    NumberOfAttempts = 1,
    Url = "https://127.0.0.1/receiver",
    AttemptInterval = 300,
    BasicAuthUsername = "tester",
    BasicAuthPassword = "Test@522",
    Expands = "changelogs,tags",
    Legacy = true,
    PostbackConfigId = "11e95f8ec39de8fbdb0a4f1a",
    ProductTransactionId = "11e95f8ec39de8fbdb0a4f1a",
};

try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.CreateanewcontactpostbackconfigAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Createanewtransactionpostbackconfig

```csharp
CreateanewtransactionpostbackconfigAsync(
    Models.V1WebhooksTransactionRequest body,
    List<Models.Expand123> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1WebhooksTransactionRequest`](../../doc/models/v1-webhooks-transaction-request.md) | Body, Required | - |
| `expand` | [`List<Expand123>`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
V1WebhooksTransactionRequest body = new V1WebhooksTransactionRequest
{
    IsActive = true,
    LocationId = "11e95f8ec39de8fbdb0a4f1a",
    OnCreate = true,
    OnUpdate = true,
    OnDelete = true,
    ProductTransactionId = "11e95f8ec39de8fbdb0a4f1a",
    NumberOfAttempts = 1,
    Url = "https://127.0.0.1/receiver",
    AttemptInterval = 300,
    BasicAuthUsername = "tester",
    BasicAuthPassword = "Test@522",
    Expands = "changelogs,tags",
    Legacy = true,
    PostbackConfigId = "11e95f8ec39de8fbdb0a4f1a",
};

try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.CreateanewtransactionpostbackconfigAsync(body);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Deleteapostbackconfig

```csharp
DeleteapostbackconfigAsync(
    string webhookId)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookId` | `string` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
string webhookId = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.DeleteapostbackconfigAsync(webhookId);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is Response401TokenException)
    {
       // TODO: Handle Response401TokenException exception here
    }
}
```

## Example Response *(as JSON)*

```json
{
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Updatetransactionbatchpostbackconfig

```csharp
UpdatetransactionbatchpostbackconfigAsync(
    string webhookId,
    Models.V1WebhooksBatchRequest1 body,
    List<Models.Expand123> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookId` | `string` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1WebhooksBatchRequest1`](../../doc/models/v1-webhooks-batch-request-1.md) | Body, Required | - |
| `expand` | [`List<Expand123>`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
string webhookId = "11e95f8ec39de8fbdb0a4f1a";
V1WebhooksBatchRequest1 body = new V1WebhooksBatchRequest1
{
    AttemptInterval = 300,
    BasicAuthUsername = "tester",
    BasicAuthPassword = "Test@522",
    Expands = "changelogs,tags",
    IsActive = true,
    LocationId = "11e95f8ec39de8fbdb0a4f1a",
    OnCreate = true,
    OnUpdate = true,
    OnDelete = true,
    Legacy = true,
    PostbackConfigId = "11e95f8ec39de8fbdb0a4f1a",
    ProductTransactionId = "11e95f8ec39de8fbdb0a4f1a",
    NumberOfAttempts = 1,
    Url = "https://127.0.0.1/receiver",
};

try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.UpdatetransactionbatchpostbackconfigAsync(
        webhookId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Updatecontactpostbackconfig

```csharp
UpdatecontactpostbackconfigAsync(
    string webhookId,
    Models.V1WebhooksContactRequest1 body,
    List<Models.Expand123> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookId` | `string` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1WebhooksContactRequest1`](../../doc/models/v1-webhooks-contact-request-1.md) | Body, Required | - |
| `expand` | [`List<Expand123>`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
string webhookId = "11e95f8ec39de8fbdb0a4f1a";
V1WebhooksContactRequest1 body = new V1WebhooksContactRequest1
{
    AttemptInterval = 300,
    BasicAuthUsername = "tester",
    BasicAuthPassword = "Test@522",
    Expands = "changelogs,tags",
    IsActive = true,
    LocationId = "11e95f8ec39de8fbdb0a4f1a",
    OnCreate = true,
    OnUpdate = true,
    OnDelete = true,
    Legacy = true,
    PostbackConfigId = "11e95f8ec39de8fbdb0a4f1a",
    ProductTransactionId = "11e95f8ec39de8fbdb0a4f1a",
    NumberOfAttempts = 1,
    Url = "https://127.0.0.1/receiver",
};

try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.UpdatecontactpostbackconfigAsync(
        webhookId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Updatetransactionpostbackconfig

```csharp
UpdatetransactionpostbackconfigAsync(
    string webhookId,
    Models.V1WebhooksTransactionRequest1 body,
    List<Models.Expand123> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `webhookId` | `string` | Template, Required | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1WebhooksTransactionRequest1`](../../doc/models/v1-webhooks-transaction-request-1.md) | Body, Required | - |
| `expand` | [`List<Expand123>`](../../doc/models/expand-123.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseWebhook](../../doc/models/response-webhook.md).

## Example Usage

```csharp
string webhookId = "11e95f8ec39de8fbdb0a4f1a";
V1WebhooksTransactionRequest1 body = new V1WebhooksTransactionRequest1
{
    AttemptInterval = 300,
    BasicAuthUsername = "tester",
    BasicAuthPassword = "Test@522",
    Expands = "changelogs,tags",
    IsActive = true,
    LocationId = "11e95f8ec39de8fbdb0a4f1a",
    OnCreate = true,
    OnUpdate = true,
    OnDelete = true,
    Legacy = true,
    PostbackConfigId = "11e95f8ec39de8fbdb0a4f1a",
    ProductTransactionId = "11e95f8ec39de8fbdb0a4f1a",
    NumberOfAttempts = 1,
    Url = "https://127.0.0.1/receiver",
};

try
{
    ApiResponse<ResponseWebhook> result = await webhooksController.UpdatetransactionpostbackconfigAsync(
        webhookId,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
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
  "type": "Webhook",
  "data": {
    "attempt_interval": 300,
    "basic_auth_username": "username",
    "basic_auth_password": "password",
    "expands": "changelogs,tags",
    "format": "api-default",
    "is_active": true,
    "location_id": "11e95f8ec39de8fbdb0a4f1a",
    "on_create": true,
    "on_update": true,
    "on_delete": true,
    "legacy": true,
    "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
    "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "resource": "contact",
    "number_of_attempts": 1,
    "url": "https://127.0.0.1/receiver",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "postback_logs": [
      {
        "id": "11e95f8ec39de8fbdb0a4f1a",
        "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
        "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
        "next_run_ts": 1422040992,
        "created_ts": 1422040992,
        "model_id": "11e95f8ec39de8fbdb0a4f1a"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

