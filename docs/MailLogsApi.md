# MailLogsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listAccessLogsV1**](#listaccesslogsv1) | **GET** /api/mail/v1/orders/{orderId}/logs/access | List access logs|
|[**listActionLogsV1**](#listactionlogsv1) | **GET** /api/mail/v1/orders/{orderId}/logs/action | List action logs|
|[**listInboundLogsV1**](#listinboundlogsv1) | **GET** /api/mail/v1/orders/{orderId}/logs/inbound | List inbound logs|
|[**listMailboxActionLogsV1**](#listmailboxactionlogsv1) | **GET** /api/mail/v1/orders/{orderId}/logs/mailbox-actions | List mailbox action logs|
|[**listOutboundLogsV1**](#listoutboundlogsv1) | **GET** /api/mail/v1/orders/{orderId}/logs/outbound | List outbound logs|

# **listAccessLogsV1**
> MailListAccessLogsV1200Response listAccessLogsV1()

Retrieve paginated access logs for the domain attached to the given mail order. Supports filtering by account, date range, protocol, status, and deletion flag. Results are sorted by timestamp descending.

### Example

```typescript
import {
    MailLogsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailLogsApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let account: string; //Filter log entries by a specific email account (optional) (default to undefined)
let date: string; //Exact date filter (YYYY-MM-DD). Takes precedence over `from_date`/`to_date` when both are given. (optional) (default to undefined)
let fromDate: string; //Date range start (RFC 3339) (optional) (default to undefined)
let toDate: string; //Date range end (RFC 3339) (optional) (default to undefined)
let status: 'Successful' | 'Failed'; //Filter log entries by status (optional) (default to undefined)
let protocol: 'imap' | 'pop3' | 'smtp'; //Filter access log entries by protocol (optional) (default to undefined)
let hasDeletions: boolean; //Filter access log entries by whether the session had deletions (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAccessLogsV1(
    orderId,
    account,
    date,
    fromDate,
    toDate,
    status,
    protocol,
    hasDeletions,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **account** | [**string**] | Filter log entries by a specific email account | (optional) defaults to undefined|
| **date** | [**string**] | Exact date filter (YYYY-MM-DD). Takes precedence over &#x60;from_date&#x60;/&#x60;to_date&#x60; when both are given. | (optional) defaults to undefined|
| **fromDate** | [**string**] | Date range start (RFC 3339) | (optional) defaults to undefined|
| **toDate** | [**string**] | Date range end (RFC 3339) | (optional) defaults to undefined|
| **status** | [**&#39;Successful&#39; | &#39;Failed&#39;**]**Array<&#39;Successful&#39; &#124; &#39;Failed&#39;>** | Filter log entries by status | (optional) defaults to undefined|
| **protocol** | [**&#39;imap&#39; | &#39;pop3&#39; | &#39;smtp&#39;**]**Array<&#39;imap&#39; &#124; &#39;pop3&#39; &#124; &#39;smtp&#39;>** | Filter access log entries by protocol | (optional) defaults to undefined|
| **hasDeletions** | [**boolean**] | Filter access log entries by whether the session had deletions | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListAccessLogsV1200Response**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listActionLogsV1**
> MailListActionLogsV1200Response listActionLogsV1()

Retrieve paginated account action logs (administrative and user actions) for the given mail order. Supports filtering by account, date range, and status. Results are sorted by timestamp descending.

### Example

```typescript
import {
    MailLogsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailLogsApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let account: string; //Filter log entries by a specific email account (optional) (default to undefined)
let date: string; //Exact date filter (YYYY-MM-DD). Takes precedence over `from_date`/`to_date` when both are given. (optional) (default to undefined)
let fromDate: string; //Date range start (RFC 3339) (optional) (default to undefined)
let toDate: string; //Date range end (RFC 3339) (optional) (default to undefined)
let status: 'Successful' | 'Failed'; //Filter log entries by status (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listActionLogsV1(
    orderId,
    account,
    date,
    fromDate,
    toDate,
    status,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **account** | [**string**] | Filter log entries by a specific email account | (optional) defaults to undefined|
| **date** | [**string**] | Exact date filter (YYYY-MM-DD). Takes precedence over &#x60;from_date&#x60;/&#x60;to_date&#x60; when both are given. | (optional) defaults to undefined|
| **fromDate** | [**string**] | Date range start (RFC 3339) | (optional) defaults to undefined|
| **toDate** | [**string**] | Date range end (RFC 3339) | (optional) defaults to undefined|
| **status** | [**&#39;Successful&#39; | &#39;Failed&#39;**]**Array<&#39;Successful&#39; &#124; &#39;Failed&#39;>** | Filter log entries by status | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListActionLogsV1200Response**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listInboundLogsV1**
> MailListInboundLogsV1200Response listInboundLogsV1()

Retrieve paginated inbound (received mail) delivery logs for the domain attached to the given mail order. Supports filtering by account, date range, status, sender, and recipient. Results are sorted by timestamp descending.

### Example

```typescript
import {
    MailLogsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailLogsApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let account: string; //Filter log entries by a specific email account (optional) (default to undefined)
let date: string; //Exact date filter (YYYY-MM-DD). Takes precedence over `from_date`/`to_date` when both are given. (optional) (default to undefined)
let fromDate: string; //Date range start (RFC 3339) (optional) (default to undefined)
let toDate: string; //Date range end (RFC 3339) (optional) (default to undefined)
let status: 'Successful' | 'Failed'; //Filter log entries by status (optional) (default to undefined)
let sender: string; //Filter log entries by sender. Accepts a full email address or a domain. (optional) (default to undefined)
let recipient: string; //Filter log entries by recipient. Accepts a full email address or a domain. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listInboundLogsV1(
    orderId,
    account,
    date,
    fromDate,
    toDate,
    status,
    sender,
    recipient,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **account** | [**string**] | Filter log entries by a specific email account | (optional) defaults to undefined|
| **date** | [**string**] | Exact date filter (YYYY-MM-DD). Takes precedence over &#x60;from_date&#x60;/&#x60;to_date&#x60; when both are given. | (optional) defaults to undefined|
| **fromDate** | [**string**] | Date range start (RFC 3339) | (optional) defaults to undefined|
| **toDate** | [**string**] | Date range end (RFC 3339) | (optional) defaults to undefined|
| **status** | [**&#39;Successful&#39; | &#39;Failed&#39;**]**Array<&#39;Successful&#39; &#124; &#39;Failed&#39;>** | Filter log entries by status | (optional) defaults to undefined|
| **sender** | [**string**] | Filter log entries by sender. Accepts a full email address or a domain. | (optional) defaults to undefined|
| **recipient** | [**string**] | Filter log entries by recipient. Accepts a full email address or a domain. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListInboundLogsV1200Response**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listMailboxActionLogsV1**
> MailListMailboxActionLogsV1200Response listMailboxActionLogsV1()

Retrieve paginated mailbox action logs (message and mailbox events) for a mailbox in the given mail order. The mailbox email must belong to the order\'s domain. Supports date range and event type filters. Results are sorted by timestamp descending.

### Example

```typescript
import {
    MailLogsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailLogsApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let email: string; //Mailbox email address. Must belong to the order\'s domain. (default to undefined)
let date: string; //Exact date filter (YYYY-MM-DD). Takes precedence over `from_date`/`to_date` when both are given. (optional) (default to undefined)
let fromDate: string; //Date range start (RFC 3339) (optional) (default to undefined)
let toDate: string; //Date range end (RFC 3339) (optional) (default to undefined)
let event: 'MessageNew' | 'MessageRead' | 'MessageAppend' | 'MessageExpunge' | 'MailboxCreate' | 'MailboxDelete' | 'MailboxRename'; //Filter mailbox action log entries by event type (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listMailboxActionLogsV1(
    orderId,
    email,
    date,
    fromDate,
    toDate,
    event,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **email** | [**string**] | Mailbox email address. Must belong to the order\&#39;s domain. | defaults to undefined|
| **date** | [**string**] | Exact date filter (YYYY-MM-DD). Takes precedence over &#x60;from_date&#x60;/&#x60;to_date&#x60; when both are given. | (optional) defaults to undefined|
| **fromDate** | [**string**] | Date range start (RFC 3339) | (optional) defaults to undefined|
| **toDate** | [**string**] | Date range end (RFC 3339) | (optional) defaults to undefined|
| **event** | [**&#39;MessageNew&#39; | &#39;MessageRead&#39; | &#39;MessageAppend&#39; | &#39;MessageExpunge&#39; | &#39;MailboxCreate&#39; | &#39;MailboxDelete&#39; | &#39;MailboxRename&#39;**]**Array<&#39;MessageNew&#39; &#124; &#39;MessageRead&#39; &#124; &#39;MessageAppend&#39; &#124; &#39;MessageExpunge&#39; &#124; &#39;MailboxCreate&#39; &#124; &#39;MailboxDelete&#39; &#124; &#39;MailboxRename&#39;>** | Filter mailbox action log entries by event type | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListMailboxActionLogsV1200Response**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listOutboundLogsV1**
> MailListInboundLogsV1200Response listOutboundLogsV1()

Retrieve paginated outbound (sent mail) delivery logs for the domain attached to the given mail order. Supports filtering by account, date range, status, sender, and recipient. Results are sorted by timestamp descending.

### Example

```typescript
import {
    MailLogsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailLogsApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let account: string; //Filter log entries by a specific email account (optional) (default to undefined)
let date: string; //Exact date filter (YYYY-MM-DD). Takes precedence over `from_date`/`to_date` when both are given. (optional) (default to undefined)
let fromDate: string; //Date range start (RFC 3339) (optional) (default to undefined)
let toDate: string; //Date range end (RFC 3339) (optional) (default to undefined)
let status: 'Successful' | 'Failed'; //Filter log entries by status (optional) (default to undefined)
let sender: string; //Filter log entries by sender. Accepts a full email address or a domain. (optional) (default to undefined)
let recipient: string; //Filter log entries by recipient. Accepts a full email address or a domain. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listOutboundLogsV1(
    orderId,
    account,
    date,
    fromDate,
    toDate,
    status,
    sender,
    recipient,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **account** | [**string**] | Filter log entries by a specific email account | (optional) defaults to undefined|
| **date** | [**string**] | Exact date filter (YYYY-MM-DD). Takes precedence over &#x60;from_date&#x60;/&#x60;to_date&#x60; when both are given. | (optional) defaults to undefined|
| **fromDate** | [**string**] | Date range start (RFC 3339) | (optional) defaults to undefined|
| **toDate** | [**string**] | Date range end (RFC 3339) | (optional) defaults to undefined|
| **status** | [**&#39;Successful&#39; | &#39;Failed&#39;**]**Array<&#39;Successful&#39; &#124; &#39;Failed&#39;>** | Filter log entries by status | (optional) defaults to undefined|
| **sender** | [**string**] | Filter log entries by sender. Accepts a full email address or a domain. | (optional) defaults to undefined|
| **recipient** | [**string**] | Filter log entries by recipient. Accepts a full email address or a domain. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListInboundLogsV1200Response**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

