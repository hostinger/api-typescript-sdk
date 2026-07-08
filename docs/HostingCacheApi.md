# HostingCacheApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**clearWebsiteCacheV1**](#clearwebsitecachev1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/cache/clear | Clear website cache|
|[**toggleCachelessModeV1**](#togglecachelessmodev1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/cacheless-mode/toggle | Toggle cacheless mode|
|[**toggleWebsiteCacheV1**](#togglewebsitecachev1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/cache/toggle | Toggle website cache|

# **clearWebsiteCacheV1**
> CommonSuccessEmptyResource clearWebsiteCacheV1()

Permanently clears all server-side cache for the website at once. Use it when content was updated and needs to be visible immediately, or after making major changes.  Also purges the Hostinger CDN cache when CDN is enabled on the website. For a WordPress installation living in a subdirectory, pass the directory query parameter to clear its cache.

### Example

```typescript
import {
    HostingCacheApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCacheApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let directory: string; //Directory of the website installation to clear, relative to the website root. Defaults to the website root. (optional) (default to undefined)

const { status, data } = await apiInstance.clearWebsiteCacheV1(
    username,
    domain,
    directory
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **directory** | [**string**] | Directory of the website installation to clear, relative to the website root. Defaults to the website root. | (optional) defaults to undefined|


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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **toggleCachelessModeV1**
> CommonSuccessEmptyResource toggleCachelessModeV1(hostingV1CacheToggleCachelessModeRequest)

Turns development (cacheless) mode on or off, based on the enabled flag. When enabled, nothing is cached, effectively turning off all caching for the website; use it while actively developing, testing changes, debugging issues, or when real-time updates must be visible. Disable it after finishing development work to restore the performance benefits of caching.

### Example

```typescript
import {
    HostingCacheApi,
    Configuration,
    HostingV1CacheToggleCachelessModeRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCacheApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1CacheToggleCachelessModeRequest: HostingV1CacheToggleCachelessModeRequest; //

const { status, data } = await apiInstance.toggleCachelessModeV1(
    username,
    domain,
    hostingV1CacheToggleCachelessModeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1CacheToggleCachelessModeRequest** | **HostingV1CacheToggleCachelessModeRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **toggleWebsiteCacheV1**
> CommonSuccessEmptyResource toggleWebsiteCacheV1(hostingV1CacheToggleCacheRequest)

Turns server-side caching for the website on or off, based on the enabled flag. Enable it for faster page loads, reduced server load, and improved user experience; recommended for production websites. Disabling may impact performance; to temporarily bypass caching while developing or debugging, prefer toggling cacheless mode instead.  Does nothing if caching is already in the requested state.

### Example

```typescript
import {
    HostingCacheApi,
    Configuration,
    HostingV1CacheToggleCacheRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCacheApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1CacheToggleCacheRequest: HostingV1CacheToggleCacheRequest; //

const { status, data } = await apiInstance.toggleWebsiteCacheV1(
    username,
    domain,
    hostingV1CacheToggleCacheRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1CacheToggleCacheRequest** | **HostingV1CacheToggleCacheRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

