# HostingRedirectsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebsiteRedirectV1**](#createwebsiteredirectv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/redirects | Create website redirect|
|[**deleteWebsiteRedirectV1**](#deletewebsiteredirectv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/redirects | Delete website redirect|
|[**listWebsiteRedirectsV1**](#listwebsiteredirectsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/redirects | List website redirects|

# **createWebsiteRedirectV1**
> HostingV1RedirectsRedirectResource createWebsiteRedirectV1(hostingV1RedirectsCreateRedirectRequest)

Creates a redirect from a URL on the selected website to another URL or IP address.

### Example

```typescript
import {
    HostingRedirectsApi,
    Configuration,
    HostingV1RedirectsCreateRedirectRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingRedirectsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1RedirectsCreateRedirectRequest: HostingV1RedirectsCreateRedirectRequest; //

const { status, data } = await apiInstance.createWebsiteRedirectV1(
    username,
    domain,
    hostingV1RedirectsCreateRedirectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1RedirectsCreateRedirectRequest** | **HostingV1RedirectsCreateRedirectRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1RedirectsRedirectResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWebsiteRedirectV1**
> CommonSuccessEmptyResource deleteWebsiteRedirectV1()

Permanently deletes the redirect identified by its source URL.  Pass the `from` value exactly as returned by the list redirects endpoint.

### Example

```typescript
import {
    HostingRedirectsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingRedirectsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let from: string; //Source URL returned by the list redirects endpoint. (default to undefined)

const { status, data } = await apiInstance.deleteWebsiteRedirectV1(
    username,
    domain,
    from
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **from** | [**string**] | Source URL returned by the list redirects endpoint. | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWebsiteRedirectsV1**
> HostingListWebsiteRedirectsV1200Response listWebsiteRedirectsV1()

Returns a paginated list of redirects configured for the selected website.

### Example

```typescript
import {
    HostingRedirectsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingRedirectsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listWebsiteRedirectsV1(
    username,
    domain,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**HostingListWebsiteRedirectsV1200Response**

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

