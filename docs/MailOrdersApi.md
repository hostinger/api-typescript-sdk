# MailOrdersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getMailOrderListV1**](#getmailorderlistv1) | **GET** /api/mail/v1/orders | Get mail order list|

# **getMailOrderListV1**
> MailGetMailOrderListV1200Response getMailOrderListV1()

Retrieve a paginated list of mail orders associated with your account.  Use this endpoint to monitor your mail services, including their status, plan, attached domain, and expiration details.

### Example

```typescript
import {
    MailOrdersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailOrdersApi(configuration);

let domain: string; //Filter orders by domain name (exact match) (optional) (default to undefined)
let status: 'pending_setup' | 'active' | 'suspended'; //Filter orders by status (optional) (default to undefined)
let isTrial: boolean; //Filter orders by trial state (optional) (default to undefined)
let sort: 'created_at' | '-created_at' | 'expires_at' | '-expires_at'; //Sort orders by field. Prefix with `-` for descending order. (optional) (default to '-created_at')
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.getMailOrderListV1(
    domain,
    status,
    isTrial,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Filter orders by domain name (exact match) | (optional) defaults to undefined|
| **status** | [**&#39;pending_setup&#39; | &#39;active&#39; | &#39;suspended&#39;**]**Array<&#39;pending_setup&#39; &#124; &#39;active&#39; &#124; &#39;suspended&#39;>** | Filter orders by status | (optional) defaults to undefined|
| **isTrial** | [**boolean**] | Filter orders by trial state | (optional) defaults to undefined|
| **sort** | [**&#39;created_at&#39; | &#39;-created_at&#39; | &#39;expires_at&#39; | &#39;-expires_at&#39;**]**Array<&#39;created_at&#39; &#124; &#39;-created_at&#39; &#124; &#39;expires_at&#39; &#124; &#39;-expires_at&#39;>** | Sort orders by field. Prefix with &#x60;-&#x60; for descending order. | (optional) defaults to '-created_at'|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailGetMailOrderListV1200Response**

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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

