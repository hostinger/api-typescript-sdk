# HostingCDNApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**disableCDNV1**](#disablecdnv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/cdn/disable | Disable CDN|
|[**enableCDNV1**](#enablecdnv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/cdn/enable | Enable CDN|
|[**getCDNStatusV1**](#getcdnstatusv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/cdn/status | Get CDN status|
|[**purgeCDNCacheV1**](#purgecdncachev1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/cdn/purge | Purge CDN cache|

# **disableCDNV1**
> CommonSuccessEmptyResource disableCDNV1()

Turns off the Hostinger CDN for the website domain. Once DNS propagation completes, the website content is served directly from the origin server. Repeating the call is safe; when CDN is already disabled, it applies the DNS change again.  Returns 422 for platform-managed domains (for example `*.hostingersite.com` and `*.app-preview.com`), where CDN cannot be disabled, even when CDN is already off. Also returns 422 while the account is being moved to another server (retry after the move finishes), or when the CDN provider rejects the change. Returns 404 when the domain is not a website on the account.

### Example

```typescript
import {
    HostingCDNApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingCDNApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.disableCDNV1(
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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableCDNV1**
> CommonSuccessEmptyResource enableCDNV1()

Turns on the Hostinger CDN for the website domain, which speeds up page loads and reduces the load on the server. Works for the main domain, parked domains and subdomains of the account.  Enabling changes the domain\'s DNS records and usually takes a few seconds. After that, DNS propagation can take a few more minutes before visitors are served through the CDN.  Repeating the call is safe, for example after a timeout. When CDN is already enabled, it applies the DNS change again and refreshes the CDN SSL certificate.  Returns 422 when the account is disabled, while the account is being moved to another server (retry after the move finishes), or when the CDN provider rejects the change. Returns 404 when the domain is not a website on the account.

### Example

```typescript
import {
    HostingCDNApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingCDNApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.enableCDNV1(
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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCDNStatusV1**
> HostingV1CdnCdnStatusResource getCDNStatusV1()

Returns whether the Hostinger CDN is enabled for the website domain. Works for the main domain, parked domains and subdomains of the account.  The domain must be the exact website name as listed on the account, without a `www.` prefix. Returns 404 when the domain is not a website on the account.

### Example

```typescript
import {
    HostingCDNApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingCDNApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getCDNStatusV1(
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

**HostingV1CdnCdnStatusResource**

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

# **purgeCDNCacheV1**
> CommonSuccessEmptyResource purgeCDNCacheV1()

Purges the website\'s content from the Hostinger CDN edge cache only. The origin server cache is not touched; to clear both, use `Clear website cache`.  Returns 422 when CDN is not enabled on the website. Returns 404 when the domain is not a website on the account.

### Example

```typescript
import {
    HostingCDNApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingCDNApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.purgeCDNCacheV1(
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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

