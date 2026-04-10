# Async Processing

```csharp
AsyncProcessingController asyncProcessingController = client.AsyncProcessingController;
```

## Class Name

`AsyncProcessingController`


# Status Check

Retrieve the current status for a particular code.

```csharp
StatusCheckAsync(
    Guid statusCode)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `statusCode` | `Guid` | Template, Required | A [UUID v4](https://datatracker.ietf.org/doc/html/rfc4122) that's unique for the Async Request |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseAsyncStatus](../../doc/models/response-async-status.md).

## Example Usage

```csharp
Guid statusCode = new Guid("406c66c3-21cb-47fb-80fc-843bc42507fb");
try
{
    ApiResponse<ResponseAsyncStatus> result = await asyncProcessingController.StatusCheckAsync(statusCode);
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
  "type": "AsyncStatus",
  "data": {
    "code": "406c66c3-21cb-47fb-80fc-843bc42507fb",
    "type": "Transaction",
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "progress": 100,
    "error": null,
    "ttl": 7956886942
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

