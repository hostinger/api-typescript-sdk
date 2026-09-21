# AgencyHostingSSLApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getWebsiteSSLStatusV1**](#getwebsitesslstatusv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/domains/{domain}/ssl/status | Get website SSL status|
|[**installWebsiteSSLV1**](#installwebsitesslv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/domains/{domain}/ssl/setup | Install website SSL|
|[**reinstallWebsiteSSLV1**](#reinstallwebsitesslv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/domains/{domain}/ssl/reinstall | Reinstall website SSL|
|[**uninstallWebsiteSSLV1**](#uninstallwebsitesslv1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid}/domains/{domain}/ssl | Uninstall website SSL|

# **getWebsiteSSLStatusV1**
> AgencyHostingV1SslSslStatusResource getWebsiteSSLStatusV1()

Returns the SSL state of one domain of an Agency Plan website: the certificate `status`, whether the certificate was uploaded by the customer, and when it stops being valid.  `installing` means a certificate setup is running or retrying; the `ssl_setup` entry of `List website processes` shows the same progress. `active` means a valid certificate is in place: uploaded by the customer, issued by the platform, or a lifetime certificate bought for the domain. `failed` means the last setup gave up and no valid certificate is in place. `expired` means the certificate has run out. `not_installed` means the domain has no certificate and no setup process. Returns 404 when the website or the domain does not exist.

### Example

```typescript
import {
    AgencyHostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingSSLApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getWebsiteSSLStatusV1(
    websiteUid,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**AgencyHostingV1SslSslStatusResource**

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

# **installWebsiteSSLV1**
> CommonSuccessEmptyResource installWebsiteSSLV1()

Starts a Let\'s Encrypt certificate setup for the domain and returns at once; the setup runs in the background. `Get website SSL status` reports `installing` while it runs, then `active` or `failed`; the `ssl_setup` entry of `List website processes` shows the same progress.  Returns 422 when the domain already has a platform certificate that is not expired, when a certificate process is recorded for the domain (a failed setup counts until it is cleaned up), or when the domain hit its limit of three setups per seven days. Returns 429 when the same domain was requested less than a minute ago, 403 when the website is suspended or locked, and 404 when the website or the domain does not exist.

### Example

```typescript
import {
    AgencyHostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingSSLApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.installWebsiteSSLV1(
    websiteUid,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
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

# **reinstallWebsiteSSLV1**
> CommonSuccessEmptyResource reinstallWebsiteSSLV1()

Replaces the Let\'s Encrypt certificate of the domain: the current platform certificate, when one is recorded, is revoked and removed, then a new setup starts in the background. Returns at once; `Get website SSL status` reports `installing` while it runs, then `active` or `failed`.  Returns 422 for free subdomains, when a certificate process is recorded for the domain (a failed setup counts until it is cleaned up), or when the domain hit its limit of three setups per seven days. Returns 429 when the same domain was requested less than a minute ago, and 403 when the website is suspended or locked, and 404 when the website or the domain does not exist.

### Example

```typescript
import {
    AgencyHostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingSSLApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.reinstallWebsiteSSLV1(
    websiteUid,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
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

# **uninstallWebsiteSSLV1**
> CommonSuccessEmptyResource uninstallWebsiteSSLV1()

Removes the platform-issued Let\'s Encrypt certificate of the domain: the certificate is revoked and deleted before the response, so the domain is no longer served with a platform certificate until a new setup completes. Also succeeds when the domain has no platform certificate to remove. Uploaded (custom) certificates are not affected.  Returns 422 when a certificate process is recorded for the domain (a failed setup counts until it is cleaned up), 429 when the same domain was requested less than a minute ago, and 403 when the website is suspended or locked, and 404 when the website or the domain does not exist.

### Example

```typescript
import {
    AgencyHostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingSSLApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.uninstallWebsiteSSLV1(
    websiteUid,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
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

