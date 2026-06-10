# HostingWebsitesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebsiteV1**](#createwebsitev1) | **POST** /api/hosting/v1/websites | Create website|
|[**listWebsitesV1**](#listwebsitesv1) | **GET** /api/hosting/v1/websites | List websites|

# **createWebsiteV1**
> CommonSuccessEmptyResource createWebsiteV1(hostingV1WebsitesCreateWebsiteRequest)

Create a new website for the authenticated client.  Provide the domain name and associated order ID to create a new website. The datacenter_code parameter is required when creating the first website on a new hosting plan - this will set up and configure new hosting account in the selected datacenter.  Subsequent websites will be hosted on the same datacenter automatically.  Website creation takes up to a few minutes to complete. Check the websites list endpoint to see when your new website becomes available.

### Example

```typescript
import {
    HostingWebsitesApi,
    Configuration,
    HostingV1WebsitesCreateWebsiteRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingWebsitesApi(configuration);

let hostingV1WebsitesCreateWebsiteRequest: HostingV1WebsitesCreateWebsiteRequest; //

const { status, data } = await apiInstance.createWebsiteV1(
    hostingV1WebsitesCreateWebsiteRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1WebsitesCreateWebsiteRequest** | **HostingV1WebsitesCreateWebsiteRequest**|  | |


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWebsitesV1**
> HostingListWebsitesV1200Response listWebsitesV1()

Retrieve a paginated list of websites (main and addon types) accessible to the authenticated client.  This endpoint returns websites from your hosting accounts as well as websites from other client hosting accounts that have shared access with you.  Use the available query parameters to filter results by username, order ID, enabled status, or domain name for more targeted results.

### Example

```typescript
import {
    HostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingWebsitesApi(configuration);

let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let username: string; //Filter by specific username (optional) (default to undefined)
let orderId: number; //Order ID (optional) (default to undefined)
let isEnabled: boolean; //Filter by enabled status (optional) (default to undefined)
let domain: string; //Filter by domain name (exact match) (optional) (default to undefined)

const { status, data } = await apiInstance.listWebsitesV1(
    page,
    perPage,
    username,
    orderId,
    isEnabled,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **username** | [**string**] | Filter by specific username | (optional) defaults to undefined|
| **orderId** | [**number**] | Order ID | (optional) defaults to undefined|
| **isEnabled** | [**boolean**] | Filter by enabled status | (optional) defaults to undefined|
| **domain** | [**string**] | Filter by domain name (exact match) | (optional) defaults to undefined|


### Return type

**HostingListWebsitesV1200Response**

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

