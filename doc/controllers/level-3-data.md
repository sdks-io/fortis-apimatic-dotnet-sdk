# Level 3 Data

```csharp
Level3DataController level3DataController = client.Level3DataController;
```

## Class Name

`Level3DataController`

## Methods

* [Createanew Level 3 Entryfora Master Card](../../doc/controllers/level-3-data.md#createanew-level-3-entryfora-master-card)
* [Createanew Level 3 Entryfora Visa](../../doc/controllers/level-3-data.md#createanew-level-3-entryfora-visa)
* [Deleteasinglelevel 3 Record](../../doc/controllers/level-3-data.md#deleteasinglelevel-3-record)
* [Viewsinglelevel 3 Record](../../doc/controllers/level-3-data.md#viewsinglelevel-3-record)


# Createanew Level 3 Entryfora Master Card

```csharp
CreateanewLevel3EntryforaMasterCardAsync(
    string transactionId,
    Models.V1TransactionsLevel3MasterCardRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transactionId` | `string` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1TransactionsLevel3MasterCardRequest`](../../doc/models/v1-transactions-level-3-master-card-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTransactionLevel3Master](../../doc/models/response-transaction-level-3-master.md).

## Example Usage

```csharp
string transactionId = "11e95f8ec39de8fbdb0a4f1a";
V1TransactionsLevel3MasterCardRequest body = new V1TransactionsLevel3MasterCardRequest
{
    Level3Data = new Level3Data3
    {
        LineItems = new List<LineItem19>
        {
            new LineItem19
            {
                Description = "cool drink",
                ProductCode = "coke12345678",
                UnitCode = "gll",
                UnitCost = 10,
                AlternateTaxId = "1234",
                DiscountAmount = 10,
                DiscountRate = 11,
                Quantity = 5,
                TaxAmount = 3,
                TaxRate = 0,
                TaxTypeApplied = "22",
                TaxTypeId = "a1",
            },
        },
        DestinationCountryCode = "840",
        DutyAmount = 0,
        FreightAmount = 0,
        NationalTax = 2,
        SalesTax = 200,
        ShipfromZipCode = "AZ12345",
        ShiptoZipCode = "MI48335",
        TaxAmount = 0,
    },
};

try
{
    ApiResponse<ResponseTransactionLevel3Master> result = await level3DataController.CreateanewLevel3EntryforaMasterCardAsync(
        transactionId,
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
  "type": "TransactionLevel3Master",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Createanew Level 3 Entryfora Visa

```csharp
CreateanewLevel3EntryforaVisaAsync(
    string transactionId,
    Models.V1TransactionsLevel3VisaRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transactionId` | `string` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `body` | [`V1TransactionsLevel3VisaRequest`](../../doc/models/v1-transactions-level-3-visa-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTransactionLevel3Visa](../../doc/models/response-transaction-level-3-visa.md).

## Example Usage

```csharp
string transactionId = "11e95f8ec39de8fbdb0a4f1a";
V1TransactionsLevel3VisaRequest body = new V1TransactionsLevel3VisaRequest
{
    Level3Data = new Level3Data4
    {
        LineItems = new List<LineItem20>
        {
            new LineItem20
            {
                Description = "cool drink",
                CommodityCode = "cc123456",
                ProductCode = "fanta123456",
                UnitCode = "gll",
                UnitCost = 3,
                DiscountAmount = 0,
                OtherTaxAmount = 0,
                Quantity = 12,
                TaxAmount = 4,
                TaxRate = 0,
            },
        },
        DestinationCountryCode = "840",
        DutyAmount = 0,
        FreightAmount = 0,
        NationalTax = 2,
        SalesTax = 200,
        ShipfromZipCode = "AZ1234",
        ShiptoZipCode = "FL1234",
        TaxAmount = 10,
        CustomerVatRegistration = "12345678",
        MerchantVatRegistration = "123456",
        OrderDate = "171006",
        SummaryCommodityCode = "C1K2",
        TaxRate = 0,
        UniqueVatRefNumber = "vat1234",
    },
};

try
{
    ApiResponse<ResponseTransactionLevel3Visa> result = await level3DataController.CreateanewLevel3EntryforaVisaAsync(
        transactionId,
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
  "type": "TransactionLevel3Visa",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Deleteasinglelevel 3 Record

```csharp
Deleteasinglelevel3RecordAsync(
    string transactionId,
    string level3Id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transactionId` | `string` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `level3Id` | `string` | Template, Required | Level 3 ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTransactionLevel3](../../doc/models/response-transaction-level-3.md).

## Example Usage

```csharp
string transactionId = "11e95f8ec39de8fbdb0a4f1a";
string level3Id = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseTransactionLevel3> result = await level3DataController.Deleteasinglelevel3RecordAsync(
        transactionId,
        level3Id
    );
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
  "type": "TransactionLevel3",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Viewsinglelevel 3 Record

```csharp
Viewsinglelevel3RecordAsync(
    string transactionId,
    string level3Id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `transactionId` | `string` | Template, Required | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `level3Id` | `string` | Template, Required | Level 3 ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTransactionLevel3](../../doc/models/response-transaction-level-3.md).

## Example Usage

```csharp
string transactionId = "11e95f8ec39de8fbdb0a4f1a";
string level3Id = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseTransactionLevel3> result = await level3DataController.Viewsinglelevel3RecordAsync(
        transactionId,
        level3Id
    );
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
  "type": "TransactionLevel3",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "level3_data": {
      "destination_country_code": "840",
      "duty_amount": 0,
      "freight_amount": 0,
      "national_tax": 2,
      "sales_tax": 200,
      "shipfrom_zip_code": "AZ1234",
      "shipto_zip_code": "FL1234",
      "tax_amount": 10,
      "tax_exempt": "0",
      "customer_vat_registration": "12345678",
      "merchant_vat_registration": "123456",
      "order_date": "171006",
      "summary_commodity_code": "C1K2",
      "tax_rate": 0,
      "unique_vat_ref_number": "vat1234",
      "line_items": [
        {
          "description": "cool drink",
          "commodity_code": "cc123456",
          "discount_amount": 0,
          "other_tax_amount": 0,
          "product_code": "fanta123456",
          "quantity": 12,
          "tax_amount": 4,
          "tax_rate": 0,
          "unit_code": "gll",
          "unit_cost": 3,
          "alternate_tax_id": "1234",
          "debit_credit": "C",
          "discount_rate": 11,
          "tax_type_applied": "22",
          "tax_type_id": "11"
        }
      ]
    }
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

