# HostingPHPApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getPHPDetailsV1**](#getphpdetailsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/php/details | Get PHP details|
|[**getPHPInfoV1**](#getphpinfov1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/php/php-info | Get PHP info|
|[**resetPHPExtensionsV1**](#resetphpextensionsv1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/php/extensions/reset | Reset PHP extensions|
|[**updatePHPExtensionsV1**](#updatephpextensionsv1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/php/extensions | Update PHP extensions|
|[**updatePHPOptionsV1**](#updatephpoptionsv1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/php/options | Update PHP options|
|[**updatePHPVersionV1**](#updatephpversionv1) | **PATCH** /api/hosting/v1/accounts/{username}/websites/{domain}/php/version | Update PHP version|

# **getPHPDetailsV1**
> HostingV1PhpPhpDetailsResource getPHPDetailsV1()

Returns the full PHP configuration for the website: current version, available versions (supported and unsupported), enabled/disabled extensions, options with their current value, default, type and the plan limit (`max`), and conflicting extension groups.  Use it to check the current PHP setup before updating the version, extensions or options.

### Example

```typescript
import {
    HostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingPHPApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getPHPDetailsV1(
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

**HostingV1PhpPhpDetailsResource**

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

# **getPHPInfoV1**
> HostingV1PhpPhpInfoResource getPHPInfoV1()

Returns the full phpinfo page (HTML) for the website.  Use it to debug PHP issues or inspect the complete PHP environment of the website.

### Example

```typescript
import {
    HostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingPHPApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getPHPInfoV1(
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

**HostingV1PhpPhpInfoResource**

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

# **resetPHPExtensionsV1**
> CommonSuccessEmptyResource resetPHPExtensionsV1()

Resets all PHP extensions of the website to their default state.  Use it to recover from extension conflicts or restore the original configuration.

### Example

```typescript
import {
    HostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingPHPApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.resetPHPExtensionsV1(
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

# **updatePHPExtensionsV1**
> CommonSuccessEmptyResource updatePHPExtensionsV1(hostingV1PhpUpdatePhpExtensionsRequest)

Enables or disables PHP extensions (modules) for the website.  Use the Get PHP details endpoint to check the current extension states before changing them.

### Example

```typescript
import {
    HostingPHPApi,
    Configuration,
    HostingV1PhpUpdatePhpExtensionsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingPHPApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1PhpUpdatePhpExtensionsRequest: HostingV1PhpUpdatePhpExtensionsRequest; //

const { status, data } = await apiInstance.updatePHPExtensionsV1(
    username,
    domain,
    hostingV1PhpUpdatePhpExtensionsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1PhpUpdatePhpExtensionsRequest** | **HostingV1PhpUpdatePhpExtensionsRequest**|  | |
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

# **updatePHPOptionsV1**
> CommonSuccessEmptyResource updatePHPOptionsV1(hostingV1PhpUpdatePhpOptionsRequest)

Updates PHP options for the website (e.g. `memory_limit`, `max_execution_time`, `upload_max_filesize`). Only provide the options you want to change, inside the `options` object.  Values above the account plan limit are silently capped to that limit, so the request can succeed with a smaller applied value. Call the Get PHP details endpoint afterwards to read the applied value.

### Example

```typescript
import {
    HostingPHPApi,
    Configuration,
    HostingV1PhpUpdatePhpOptionsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingPHPApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1PhpUpdatePhpOptionsRequest: HostingV1PhpUpdatePhpOptionsRequest; //

const { status, data } = await apiInstance.updatePHPOptionsV1(
    username,
    domain,
    hostingV1PhpUpdatePhpOptionsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1PhpUpdatePhpOptionsRequest** | **HostingV1PhpUpdatePhpOptionsRequest**|  | |
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

# **updatePHPVersionV1**
> CommonSuccessEmptyResource updatePHPVersionV1(hostingV1PhpUpdatePhpVersionRequest)

Changes the PHP version of the website.  Use the Get PHP details endpoint to see the versions available for the website.

### Example

```typescript
import {
    HostingPHPApi,
    Configuration,
    HostingV1PhpUpdatePhpVersionRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingPHPApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1PhpUpdatePhpVersionRequest: HostingV1PhpUpdatePhpVersionRequest; //

const { status, data } = await apiInstance.updatePHPVersionV1(
    username,
    domain,
    hostingV1PhpUpdatePhpVersionRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1PhpUpdatePhpVersionRequest** | **HostingV1PhpUpdatePhpVersionRequest**|  | |
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

