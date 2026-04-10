# Full Boarding

```csharp
FullBoardingController fullBoardingController = client.FullBoardingController;
```

## Class Name

`FullBoardingController`


# Merchant Boarding Full

This method is used to fully board a merchant to the platform. When using this method, you must provide data for each "Required" property. See the description for each of these properties for more information about their requirement criteria.

```csharp
MerchantBoardingFullAsync(
    Models.V1FullboardingRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1FullboardingRequest`](../../doc/models/v1-fullboarding-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseFullboarding](../../doc/models/response-fullboarding.md).

## Example Usage

```csharp
V1FullboardingRequest body = new V1FullboardingRequest
{
    Email = "email@domain.com",
    DbaName = "Discount Home Goods",
    PhoneNumber = "5555551234",
    OwnershipType = OwnershipType.Np,
    FedTaxId = "0000000000",
    AverageTicket = 15,
    HighTicket = 150,
    CcMonthlyVolume = 100,
    MccCode = "7629",
    BusinessDescription = "Yard services.",
    SwipedPercent = 0,
    KeyedPercent = 0,
    EcommercePercent = 100,
    IsForeignEntity = true,
    PersonallyGuaranteed = false,
    Addresses = new List<Address81>
    {
        new Address81
        {
            AddressLine1 = "121 E Main",
            City = "Dallas",
            StateProvince = "TX",
            PostalCode = "75087",
            CountryCode = "US",
            AddressType = AddressType.Corporate,
            AddressLine2 = "Apt 707",
        },
    },
    Owners = new List<Owner>
    {
        new Owner
        {
            FirstName = "James",
            LastName = "Bond",
            Title = "CEO",
            DateOfBirth = "2021-12-01",
            AddressLine1 = "133 S Goliad St",
            AddressLine2 = "Suite 120",
            City = "Rockwall",
            StateProvince = "TX",
            PostalCode = "75429",
            CountryCode = "US",
            Ssn = "000000000",
            OwnershipPercent = 100,
            PhoneNumber = "9042142323",
            EmailAddress = "james@example.com",
            IsController = true,
            IsSigner = true,
            MiddleName = "Tyler",
        },
    },
    BankAccounts = new List<BankAccount1>
    {
        new BankAccount1
        {
            AccountHolderName = "James Bond",
            RoutingNumber = "111111111",
            AccountNumber = "1234567",
            AccountType = AccountType12.Checking,
            IsPrimary = true,
        },
    },
    TemplateId = "1234YourTemplateCode",
    ClientAppId = "ABC123",
    LegalName = "Total Home Goods, LLP",
    Website = "http://www.example.com",
    EcMonthlyVolume = 22,
    SignerIp = "192.168.0.10",
};

try
{
    ApiResponse<ResponseFullboarding> result = await fullBoardingController.MerchantBoardingFullAsync(body);
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
  "type": "Fullboarding",
  "data": {
    "result": {
      "client_app_id": "ABC123",
      "dba_name": "Discount Home Goods",
      "email": "jtodd@example.com"
    },
    "status": {
      "response_code": "Received"
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |

