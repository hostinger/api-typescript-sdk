# WordPressObjectCacheApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**showMemcachedObjectCacheStatusV1**](#showmemcachedobjectcachestatusv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/memcached/status | Show Memcached object cache status|
|[**toggleMemcachedObjectCacheV1**](#togglememcachedobjectcachev1) | **PATCH** /api/hosting/v1/accounts/{username}/wordpress/{software}/memcached/toggle | Toggle Memcached object cache|

# **showMemcachedObjectCacheStatusV1**
> WordPressV1MemcachedMemcachedStatusResource showMemcachedObjectCacheStatusV1()

Show the Memcached object cache status for the specified WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressObjectCacheApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressObjectCacheApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.showMemcachedObjectCacheStatusV1(
    username,
    software
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|


### Return type

**WordPressV1MemcachedMemcachedStatusResource**

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

# **toggleMemcachedObjectCacheV1**
> CommonSuccessEmptyResource toggleMemcachedObjectCacheV1(wordPressV1MemcachedToggleMemcachedRequest)

Activate or deactivate the Memcached object cache for the specified WordPress installation, based on the `enabled` flag.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressObjectCacheApi,
    Configuration,
    WordPressV1MemcachedToggleMemcachedRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressObjectCacheApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1MemcachedToggleMemcachedRequest: WordPressV1MemcachedToggleMemcachedRequest; //

const { status, data } = await apiInstance.toggleMemcachedObjectCacheV1(
    username,
    software,
    wordPressV1MemcachedToggleMemcachedRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1MemcachedToggleMemcachedRequest** | **WordPressV1MemcachedToggleMemcachedRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|


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

