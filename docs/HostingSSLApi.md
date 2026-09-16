# HostingSSLApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getSSLStatusV1**](#getsslstatusv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/ssl/status | Get SSL status|
|[**installSSLV1**](#installsslv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/ssl/setup | Install SSL|
|[**toggleHTTPSRedirectV1**](#togglehttpsredirectv1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/ssl/https-redirect/toggle | Toggle HTTPS redirect|
|[**uninstallSSLV1**](#uninstallsslv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/ssl | Uninstall SSL|

# **getSSLStatusV1**
> HostingV1SslSslStatusResource getSSLStatusV1()

Returns the SSL state of the website: the certificate `status` and `provider`, whether the certificate is a lifetime one managed by the platform, whether HTTP requests are redirected to HTTPS, when the certificate stops being valid and the last installation error.  `installing` and `waiting_for_retry` mean an installation is in progress. `failed` means the last installation gave up, or the website was not updated for 60 minutes while `installing`; `last_error` holds the reason when it is a known message, otherwise it is null. `expired` means the assigned certificate\'s validity has ended. `not_installed` means no certificate is assigned. Free subdomains use a platform-managed certificate: with no installation recorded they report `active` with `provider` and `expires_at` null.

### Example

```typescript
import {
    HostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingSSLApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getSSLStatusV1(
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

**HostingV1SslSslStatusResource**

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

# **installSSLV1**
> CommonSuccessEmptyResource installSSLV1()

Requests a lifetime SSL certificate for the website. The installation runs in the background; `Get SSL status` reports `active` or `failed` when it ends. An `active` lifetime certificate does not block the request: a new installation is requested, which is how a certificate is reinstalled.  Returns 422 for free subdomains (their certificate is managed by the platform), while an installation is `installing` or `waiting_for_retry`, when the website\'s certificate was revoked (it cannot be reissued), and when an uploaded custom certificate is installed; that one has to be uninstalled first.

### Example

```typescript
import {
    HostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingSSLApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.installSSLV1(
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

# **toggleHTTPSRedirectV1**
> CommonSuccessEmptyResource toggleHTTPSRedirectV1(hostingV1SslToggleHttpsRedirectRequest)

Turns the HTTP to HTTPS redirect of the website on or off, based on `is_enabled`. Does nothing when the redirect is already in the requested state. Turning it on requires an installed certificate (`status` `active` or `expired` on `Get SSL status`) and returns 422 when there is none; turning it off is always accepted.

### Example

```typescript
import {
    HostingSSLApi,
    Configuration,
    HostingV1SslToggleHttpsRedirectRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingSSLApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1SslToggleHttpsRedirectRequest: HostingV1SslToggleHttpsRedirectRequest; //

const { status, data } = await apiInstance.toggleHTTPSRedirectV1(
    username,
    domain,
    hostingV1SslToggleHttpsRedirectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1SslToggleHttpsRedirectRequest** | **HostingV1SslToggleHttpsRedirectRequest**|  | |
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

# **uninstallSSLV1**
> CommonSuccessEmptyResource uninstallSSLV1()

Removes the SSL certificate assigned to the website, turns the HTTPS redirect off and cancels a pending installation retry. The website serves plain HTTP until a new installation completes. `Get SSL status` reports `not_installed` as soon as the call returns; the call also succeeds when no certificate is assigned, so repeating it is safe.  Returns 422 for free subdomains (their certificate is managed by the platform) and while an installation is `installing`.

### Example

```typescript
import {
    HostingSSLApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingSSLApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.uninstallSSLV1(
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

