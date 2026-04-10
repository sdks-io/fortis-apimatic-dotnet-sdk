# Declined Recurring Transactions

```csharp
DeclinedRecurringTransactionsController declinedRecurringTransactionsController = client.DeclinedRecurringTransactionsController;
```

## Class Name

`DeclinedRecurringTransactionsController`

## Methods

* [Getone Declined Recurring Transaction](../../doc/controllers/declined-recurring-transactions.md#getone-declined-recurring-transaction)
* [Listall Declined Recurring Transactions](../../doc/controllers/declined-recurring-transactions.md#listall-declined-recurring-transactions)
* [Createapayment](../../doc/controllers/declined-recurring-transactions.md#createapayment)
* [Rerunthetransaction](../../doc/controllers/declined-recurring-transactions.md#rerunthetransaction)
* [Resendthetransaction](../../doc/controllers/declined-recurring-transactions.md#resendthetransaction)


# Getone Declined Recurring Transaction

```csharp
GetoneDeclinedRecurringTransactionAsync(
    string declinedRecurringTransactionId,
    List<Models.Expand5> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declinedRecurringTransactionId` | `string` | Template, Required | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`List<Expand5>`](../../doc/models/expand-5.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseDeclinedRecurringTransaction](../../doc/models/response-declined-recurring-transaction.md).

## Example Usage

```csharp
string declinedRecurringTransactionId = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseDeclinedRecurringTransaction> result = await declinedRecurringTransactionsController.GetoneDeclinedRecurringTransactionAsync(declinedRecurringTransactionId);
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
  "type": "DeclinedRecurringTransaction",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status": "paid",
    "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_ts": 1422040992,
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Listall Declined Recurring Transactions

```csharp
ListallDeclinedRecurringTransactionsAsync(
    Models.Page1 page = null,
    List<Models.Order21> order = null,
    List<Models.FilterBy> filterBy = null,
    List<Models.Expand5> expand = null,
    Models.Format1? format = null,
    string typeahead = null,
    List<Models.Field30> fields = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | [`Page1`](../../doc/models/page-1.md) | Query, Optional | Use this field to specify paginate your results, by using page size and number. You can use one of the following methods:<br><br>> /endpoint?page={ "number": 1, "size": 50 }<br>> <br>> /endpoint?page[number]=1&page[size]=50 |
| `order` | [`List<Order21>`](../../doc/models/order-21.md) | Query, Optional | Criteria used in query string parameters to order results.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`.  Must be encoded, or use syntax that does not require encoding.<br><br>> /endpoint?order[0][key]=created_ts&order[0][operator]=asc<br>> <br>> /endpoint?order=[{ "key": "created_ts", "operator": "asc"}]<br>> <br>> /endpoint?order=[{ "key": "balance", "operator": "desc"},{ "key": "created_ts", "operator": "asc"}]<br><br>**Constraints**: *Minimum Items*: `1` |
| `filterBy` | [`List<FilterBy>`](../../doc/models/filter-by.md) | Query, Optional | Filter criteria that can be used in query string parameters.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`. Must be encoded, or use syntax that does not require encoding.<br><br>> ?filter_by[0][key]=first_name&filter_by[0][operator]==&filter_by[0][value]=Steve<br>> <br>> /endpoint?filter_by=[{ "key": "first_name", "operator": "=", "value": "Fred" }]<br>> <br>> /endpoint?filter_by=[{ "key": "account_type", "operator": "=", "value": "VISA" }]<br>> <br>> /endpoint?filter_by=[{ "key": "created_ts", "operator": ">=", "value": "946702799" }, { "key": "created_ts", "operator": "<=", value: "1695061891" }]<br>> <br>> /endpoint?filter_by=[{ "key": "last_name", "operator": "IN", "value": "Williams,Brown,Allman" }]<br><br>**Constraints**: *Minimum Items*: `1` |
| `expand` | [`List<Expand5>`](../../doc/models/expand-5.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `format` | [`Format1?`](../../doc/models/format-1.md) | Query, Optional | Reporting format, valid values: csv, tsv |
| `typeahead` | `string` | Query, Optional | You can use any `field_name` from this endpoint results to order the list using the value provided as filter for the same `field_name`. It will be ordered using the following rules: 1) Exact match, 2) Starts with, 3) Contains.<br><br>> /endpoint?filter={ "field_name": "Value" }&_typeahead=field_name |
| `fields` | [`List<Field30>`](../../doc/models/field-30.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseDeclinedRecurringTransactionsCollection](../../doc/models/response-declined-recurring-transactions-collection.md).

## Example Usage

```csharp
Page1 page = new Page1
{
    Number = 1,
    Size = 50,
};

List<Order21> order = new List<Order21>
{
    new Order21
    {
        Key = "first_name",
        MOperator = Operator.Asc,
    },
};

List<FilterBy> filterBy = new List<FilterBy>
{
    new FilterBy
    {
        Key = "first_name",
        MOperator = FilterByOperator.FromOperator1(Operator1.Enum1),
        MValue = FilterByValue.FromFilterByValueCase1(
            FilterByValueCase1.FromString("Fred")
        ),
    },
};

try
{
    ApiResponse<ResponseDeclinedRecurringTransactionsCollection> result = await declinedRecurringTransactionsController.ListallDeclinedRecurringTransactionsAsync(
        page,
        order,
        filterBy
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
  "type": "DeclinedRecurringTransactionsCollection",
  "list": [
    {
      "id": "11e95f8ec39de8fbdb0a4f1a",
      "status": "paid",
      "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
      "created_ts": 1422040992,
      "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
      "modified_ts": 1422040992,
      "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
    }
  ],
  "links": {
    "type": "Links",
    "first": "/v1/endpoint?page[size]=10&page[number]=1",
    "previous": "/v1/endpoint?page[size]=10&page[number]=5",
    "next": "/v1/endpoint?page[size]=10&page[number]=7",
    "last": "/v1/endpoint?page[size]=10&page[number]=42"
  },
  "pagination": {
    "type": "Pagination",
    "total_count": 423,
    "page_count": 42,
    "page_number": 6,
    "page_size": 10
  },
  "sort": {
    "type": "Sorting",
    "fields": [
      {
        "field": "last_name",
        "order": "asc"
      }
    ]
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Createapayment

```csharp
CreateapaymentAsync(
    Models.V1DeclinedRecurringTransactionPaymentsRequest body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1DeclinedRecurringTransactionPaymentsRequest`](../../doc/models/v1-declined-recurring-transaction-payments-request.md) | Body, Required | - |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseDeclinedRecurringTransactionPayment](../../doc/models/response-declined-recurring-transaction-payment.md).

## Example Usage

```csharp
V1DeclinedRecurringTransactionPaymentsRequest body = new V1DeclinedRecurringTransactionPaymentsRequest
{
    DeclinedRecurringTransactionId = "11e95f8ec39de8fbdb0a4f1a",
    AccountNumber = "5454545454545454",
    ExpDate = "0722",
    TransactionAmount = 0,
    AccountHolderName = "John Doe",
    Description = "Description",
    SaveAccountTitle = "John Account",
    SubtotalAmount = 599,
    SurchargeAmount = 599,
};

try
{
    ApiResponse<ResponseDeclinedRecurringTransactionPayment> result = await declinedRecurringTransactionsController.CreateapaymentAsync(body);
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
  "type": "DeclinedRecurringTransactionPayment",
  "data": {
    "declined_recurring_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
    "account_number": "5454545454545454",
    "account_holder_name": "John Doe",
    "exp_date": "0722",
    "transaction_amount": 0,
    "description": "Description",
    "billing_address": {
      "postal_code": "48375",
      "city": "Novi",
      "state": "Michigan",
      "phone": "3339998822",
      "country": "USA"
    },
    "tags": [
      "Walk-in Customer"
    ],
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "first_six": "700953",
    "last_four": "3657",
    "routing": null,
    "reason_code_id": 1000,
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |
| 412 | Precondition Failed | [`Response412Exception`](../../doc/models/response-412-exception.md) |


# Rerunthetransaction

```csharp
RerunthetransactionAsync(
    string declinedRecurringTransactionId,
    List<Models.Expand5> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declinedRecurringTransactionId` | `string` | Template, Required | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`List<Expand5>`](../../doc/models/expand-5.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseDeclinedRecurringTransaction](../../doc/models/response-declined-recurring-transaction.md).

## Example Usage

```csharp
string declinedRecurringTransactionId = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseDeclinedRecurringTransaction> result = await declinedRecurringTransactionsController.RerunthetransactionAsync(declinedRecurringTransactionId);
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
  "type": "DeclinedRecurringTransaction",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "status": "paid",
    "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
    "modified_ts": 1422040992,
    "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |


# Resendthetransaction

```csharp
ResendthetransactionAsync(
    string declinedRecurringTransactionId)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declinedRecurringTransactionId` | `string` | Template, Required | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseDeclinedRecurringTransactionResend](../../doc/models/response-declined-recurring-transaction-resend.md).

## Example Usage

```csharp
string declinedRecurringTransactionId = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseDeclinedRecurringTransactionResend> result = await declinedRecurringTransactionsController.ResendthetransactionAsync(declinedRecurringTransactionId);
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
  "type": "DeclinedRecurringTransactionResend",
  "data": {
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "email_log_id": "11e95f8ec39de8fbdb0a4f1a",
    "email": "email@domain.com"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

