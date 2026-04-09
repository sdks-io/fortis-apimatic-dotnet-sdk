# Payment Card Reader Token

```csharp
PaymentCardReaderTokenController paymentCardReaderTokenController = client.PaymentCardReaderTokenController;
```

## Class Name

`PaymentCardReaderTokenController`


# Payment Card Reader Token Request

For initializing iPhone card readers for Apple Tap to Pay transactions

```csharp
PaymentCardReaderTokenRequestAsync(
    string productTransactionId)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `productTransactionId` | `string` | Query, Required | Product Transaction ID to be used to initialize the card reader<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

[`Task<Models.ResponsePaymentCardReaderToken>`](../../doc/models/response-payment-card-reader-token.md)

## Example Usage

```csharp
string productTransactionId = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ResponsePaymentCardReaderToken result = await paymentCardReaderTokenController.PaymentCardReaderTokenRequestAsync(productTransactionId);
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
    if (e is Response401tokenException)
    {
       // TODO: Handle Response401tokenException exception here
    }
}
```

## Example Response *(as JSON)*

```json
{
  "type": "PaymentCardReaderToken",
  "data": {}
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |

