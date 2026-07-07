# HostingCacheApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**clearWebsiteCacheV1**](#clearwebsitecachev1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/cache/clear | Clear website cache|
|[**disableCachelessModeV1**](#disablecachelessmodev1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/cacheless-mode/disable | Disable cacheless mode|
|[**disableWebsiteCacheV1**](#disablewebsitecachev1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/cache/disable | Disable website cache|
|[**enableCachelessModeV1**](#enablecachelessmodev1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/cacheless-mode/enable | Enable cacheless mode|
|[**enableWebsiteCacheV1**](#enablewebsitecachev1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/cache/enable | Enable website cache|

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

# **disableCachelessModeV1**
> CommonSuccessEmptyResource disableCachelessModeV1()

Turns off development (cacheless) mode and returns the website to normal caching. Use it after finishing development work to restore the performance benefits of caching.

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

const { status, data } = await apiInstance.disableCachelessModeV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **disableWebsiteCacheV1**
> CommonSuccessEmptyResource disableWebsiteCacheV1()

Turns off server-side caching for the website until it is enabled again. May impact performance. Use it when experiencing cache-related issues; to temporarily bypass caching while developing or debugging, prefer enabling cacheless mode instead.  Does nothing if caching is already disabled.

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

const { status, data } = await apiInstance.disableWebsiteCacheV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **enableCachelessModeV1**
> CommonSuccessEmptyResource enableCachelessModeV1()

Enables development (cacheless) mode where nothing is cached, effectively turning off all caching for the website. Use it while actively developing, testing changes, debugging issues, or when real-time updates must be visible. Disable cacheless mode afterwards to restore normal caching.

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

const { status, data } = await apiInstance.enableCachelessModeV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **enableWebsiteCacheV1**
> CommonSuccessEmptyResource enableWebsiteCacheV1()

Turns on server-side caching for the website for better performance. Use it for faster page loads, reduced server load, or improved user experience. Recommended for production websites.  Does nothing if caching is already enabled.

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

const { status, data } = await apiInstance.enableWebsiteCacheV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

