# Tickets

The tickets endpoint is used as a single use cc only token generation endpoint. If there is a need to store card numbers with cvv for a one time use, then this is the endpoint to perform that task.  Transactions run with the generated ticket_id can save card information for later with save_account.

```csharp
TicketsController ticketsController = client.TicketsController;
```

## Class Name

`TicketsController`

## Methods

* [Createa Ticketrecord](../../doc/controllers/tickets.md#createa-ticketrecord)
* [Listallticketsrelated](../../doc/controllers/tickets.md#listallticketsrelated)
* [Viewsingleticketrecord](../../doc/controllers/tickets.md#viewsingleticketrecord)


# Createa Ticketrecord

```csharp
CreateaTicketrecordAsync(
    Models.V1TicketsRequest body,
    List<Models.Expand44> expand = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`V1TicketsRequest`](../../doc/models/v1-tickets-request.md) | Body, Required | - |
| `expand` | [`List<Expand44>`](../../doc/models/expand-44.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTicket](../../doc/models/response-ticket.md).

## Example Usage

```csharp
V1TicketsRequest body = new V1TicketsRequest
{
    ExpDate = "0722",
    AccountNumber = "545454545454545",
    AccountHolderName = "John Smith",
    ContactId = "11e95f8ec39de8fbdb0a4f1a",
};

try
{
    ApiResponse<ResponseTicket> result = await ticketsController.CreateaTicketrecordAsync(body);
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
  "type": "Ticket",
  "data": {
    "account_holder_name": "John Smith",
    "exp_date": "0722",
    "cvv": null,
    "account_number": "545454545454545",
    "billing_address": {
      "postal_code": "48375"
    },
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "location_api_id": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
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


# Listallticketsrelated

```csharp
ListallticketsrelatedAsync(
    Models.Page1 page = null,
    List<Models.Order21> order = null,
    List<Models.FilterBy> filterBy = null,
    List<Models.Expand44> expand = null,
    Models.Format1? format = null,
    string typeahead = null,
    List<Models.Field51> fields = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `page` | [`Page1`](../../doc/models/page-1.md) | Query, Optional | Use this field to specify paginate your results, by using page size and number. You can use one of the following methods:<br><br>> /endpoint?page={ "number": 1, "size": 50 }<br>> <br>> /endpoint?page[number]=1&page[size]=50 |
| `order` | [`List<Order21>`](../../doc/models/order-21.md) | Query, Optional | Criteria used in query string parameters to order results.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`.  Must be encoded, or use syntax that does not require encoding.<br><br>> /endpoint?order[0][key]=created_ts&order[0][operator]=asc<br>> <br>> /endpoint?order=[{ "key": "created_ts", "operator": "asc"}]<br>> <br>> /endpoint?order=[{ "key": "balance", "operator": "desc"},{ "key": "created_ts", "operator": "asc"}]<br><br>**Constraints**: *Minimum Items*: `1` |
| `filterBy` | [`List<FilterBy>`](../../doc/models/filter-by.md) | Query, Optional | Filter criteria that can be used in query string parameters.  Most fields from the endpoint results can be used as a `key`.  Unsupported fields or operators will return a `412`. Must be encoded, or use syntax that does not require encoding.<br><br>> ?filter_by[0][key]=first_name&filter_by[0][operator]==&filter_by[0][value]=Steve<br>> <br>> /endpoint?filter_by=[{ "key": "first_name", "operator": "=", "value": "Fred" }]<br>> <br>> /endpoint?filter_by=[{ "key": "account_type", "operator": "=", "value": "VISA" }]<br>> <br>> /endpoint?filter_by=[{ "key": "created_ts", "operator": ">=", "value": "946702799" }, { "key": "created_ts", "operator": "<=", value: "1695061891" }]<br>> <br>> /endpoint?filter_by=[{ "key": "last_name", "operator": "IN", "value": "Williams,Brown,Allman" }]<br><br>**Constraints**: *Minimum Items*: `1` |
| `expand` | [`List<Expand44>`](../../doc/models/expand-44.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `format` | [`Format1?`](../../doc/models/format-1.md) | Query, Optional | Reporting format, valid values: csv, tsv |
| `typeahead` | `string` | Query, Optional | You can use any `field_name` from this endpoint results to order the list using the value provided as filter for the same `field_name`. It will be ordered using the following rules: 1) Exact match, 2) Starts with, 3) Contains.<br><br>> /endpoint?filter={ "field_name": "Value" }&_typeahead=field_name |
| `fields` | [`List<Field51>`](../../doc/models/field-51.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTicketsCollection](../../doc/models/response-tickets-collection.md).

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
    ApiResponse<ResponseTicketsCollection> result = await ticketsController.ListallticketsrelatedAsync(
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
  "type": "TicketsCollection",
  "list": [
    {
      "account_holder_name": "John Smith",
      "exp_date": "0722",
      "cvv": null,
      "account_number": "545454545454545",
      "billing_address": {
        "postal_code": "48375"
      },
      "contact_id": "11e95f8ec39de8fbdb0a4f1a",
      "location_api_id": null,
      "id": "11e95f8ec39de8fbdb0a4f1a",
      "created_ts": 1422040992,
      "created_user_id": "11e95f8ec39de8fbdb0a4f1a"
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


# Viewsingleticketrecord

```csharp
ViewsingleticketrecordAsync(
    string ticketId,
    List<Models.Expand44> expand = null,
    List<Models.Field51> fields = null)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ticketId` | `string` | Template, Required | A unique, system-generated identifier for the Ticket.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expand` | [`List<Expand44>`](../../doc/models/expand-44.md) | Query, Optional | Most endpoints in the API have a way to retrieve extra data related to the current record being retrieved. For example, if the API request is for the accountvaults endpoint, and the end user also needs to know which contact the token belongs to, this data can be returned in the accountvaults endpoint request.<br><br>**Constraints**: *Unique Items Required* |
| `fields` | [`List<Field51>`](../../doc/models/field-51.md) | Query, Optional | You can use any `field_name` from this endpoint results to filter the list of fields returned on the response. |

## Response Type

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ResponseTicket](../../doc/models/response-ticket.md).

## Example Usage

```csharp
string ticketId = "11e95f8ec39de8fbdb0a4f1a";
try
{
    ApiResponse<ResponseTicket> result = await ticketsController.ViewsingleticketrecordAsync(ticketId);
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
  "type": "Ticket",
  "data": {
    "account_holder_name": "John Smith",
    "exp_date": "0722",
    "cvv": null,
    "account_number": "545454545454545",
    "billing_address": {
      "postal_code": "48375"
    },
    "contact_id": "11e95f8ec39de8fbdb0a4f1a",
    "location_api_id": null,
    "id": "11e95f8ec39de8fbdb0a4f1a",
    "created_ts": 1422040992,
    "created_user_id": "11e95f8ec39de8fbdb0a4f1a"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401TokenException`](../../doc/models/response-401-token-exception.md) |

