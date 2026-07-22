# MailMailboxesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getMailboxListV1**](#getmailboxlistv1) | **GET** /api/mail/v1/orders/{orderId}/mailboxes | Get mailbox list|

# **getMailboxListV1**
> MailGetMailboxListV1200Response getMailboxListV1()

Retrieve a paginated list of mailboxes belonging to a mail order.  Use this endpoint to monitor mailboxes of your mail service, including their status, enabled protocols, attached resource counts, and periodically synced usage numbers (usage may lag behind live values).

### Example

```typescript
import {
    MailMailboxesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailMailboxesApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let search: string; //Filter mailboxes whose email address contains the given string (optional) (default to undefined)
let sort: 'address' | '-address'; //Sort mailboxes by field. Prefix with `-` for descending order. (optional) (default to 'address')
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.getMailboxListV1(
    orderId,
    search,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **search** | [**string**] | Filter mailboxes whose email address contains the given string | (optional) defaults to undefined|
| **sort** | [**&#39;address&#39; | &#39;-address&#39;**]**Array<&#39;address&#39; &#124; &#39;-address&#39;>** | Sort mailboxes by field. Prefix with &#x60;-&#x60; for descending order. | (optional) defaults to 'address'|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailGetMailboxListV1200Response**

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

