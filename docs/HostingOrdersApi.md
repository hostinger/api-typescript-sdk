# HostingOrdersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listOrdersV1**](#listordersv1) | **GET** /api/hosting/v1/orders | List orders|

# **listOrdersV1**
> HostingListOrdersV1200Response listOrdersV1()

Retrieve a paginated list of orders accessible to the authenticated client.  This endpoint returns orders of your hosting accounts as well as orders of other client hosting accounts that have shared access with you.  Use the available query parameters to filter results by order statuses or specific order IDs for more targeted results.

### Example

```typescript
import {
    HostingOrdersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingOrdersApi(configuration);

let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let statuses: Array<'active' | 'deleting' | 'deleted' | 'suspended'>; //Filter by order statuses (optional) (default to undefined)
let orderIds: Array<number>; //Filter by specific order IDs (optional) (default to undefined)

const { status, data } = await apiInstance.listOrdersV1(
    page,
    perPage,
    statuses,
    orderIds
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **statuses** | **Array<&#39;active&#39; &#124; &#39;deleting&#39; &#124; &#39;deleted&#39; &#124; &#39;suspended&#39;>** | Filter by order statuses | (optional) defaults to undefined|
| **orderIds** | **Array&lt;number&gt;** | Filter by specific order IDs | (optional) defaults to undefined|


### Return type

**HostingListOrdersV1200Response**

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
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

