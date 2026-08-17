# AgencyHostingPHPApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listAvailablePHPVersionsForAWebsiteV1**](#listavailablephpversionsforawebsitev1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/php-settings/versions | List available PHP versions for a website|
|[**listAvailablePHPVersionsForAnOrderV1**](#listavailablephpversionsforanorderv1) | **GET** /api/agency-hosting/v1/orders/{order_id}/websites/php-settings/versions | List available PHP versions for an order|
|[**listPHPExtensionsForAWebsiteV1**](#listphpextensionsforawebsitev1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/php-settings/extensions | List PHP extensions for a website|
|[**listPHPOptionsForAWebsiteV1**](#listphpoptionsforawebsitev1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/php-settings/options | List PHP options for a website|
|[**replaceWebsitePHPExtensionsV1**](#replacewebsitephpextensionsv1) | **PUT** /api/agency-hosting/v1/websites/{website_uid}/php-settings/extensions | Replace website PHP extensions|
|[**replaceWebsitePHPOptionsV1**](#replacewebsitephpoptionsv1) | **PUT** /api/agency-hosting/v1/websites/{website_uid}/php-settings/options | Replace website PHP options|
|[**updateWebsitePHPVersionV1**](#updatewebsitephpversionv1) | **PATCH** /api/agency-hosting/v1/websites/{website_uid}/php-settings/version | Update website PHP version|

# **listAvailablePHPVersionsForAWebsiteV1**
> Array<AgencyHostingV1PhpVersionResource> listAvailablePHPVersionsForAWebsiteV1()

Lists the PHP versions an Agency Plan website can be switched to. The version the website is currently running is returned as settings.php.version by the website details endpoint.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.listAvailablePHPVersionsForAWebsiteV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**Array<AgencyHostingV1PhpVersionResource>**

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

# **listAvailablePHPVersionsForAnOrderV1**
> Array<AgencyHostingV1PhpVersionResource> listAvailablePHPVersionsForAnOrderV1()

Lists the PHP versions available to websites created under an Agency Plan order, determined by the server the order is hosted on. Use this before creating a website; for a website that already exists, call the website-scoped versions endpoint instead.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let orderId: number; //Agency Plan order ID (default to undefined)

const { status, data } = await apiInstance.listAvailablePHPVersionsForAnOrderV1(
    orderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Agency Plan order ID | defaults to undefined|


### Return type

**Array<AgencyHostingV1PhpVersionResource>**

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

# **listPHPExtensionsForAWebsiteV1**
> Array<AgencyHostingV1PhpExtensionResource> listPHPExtensionsForAWebsiteV1()

Lists every PHP extension available to an Agency Plan website and whether it is currently enabled.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.listPHPExtensionsForAWebsiteV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**Array<AgencyHostingV1PhpExtensionResource>**

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

# **listPHPOptionsForAWebsiteV1**
> Array<AgencyHostingV1PhpOptionResource> listPHPOptionsForAWebsiteV1()

Lists the php.ini directives that can be configured for an Agency Plan website, each with its default, the value currently in effect, and the values it accepts.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.listPHPOptionsForAWebsiteV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**Array<AgencyHostingV1PhpOptionResource>**

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

# **replaceWebsitePHPExtensionsV1**
> CommonSuccessEmptyResource replaceWebsitePHPExtensionsV1(agencyHostingV1PhpUpdateExtensionsRequest)

Replaces the set of PHP extensions enabled on an Agency Plan website with the ones provided. Any toggleable extension not in the request is disabled, so call the extensions endpoint first and send the full desired set. Extensions compiled into PHP, reported with the \"built-in\" state, are always active and are unaffected.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration,
    AgencyHostingV1PhpUpdateExtensionsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1PhpUpdateExtensionsRequest: AgencyHostingV1PhpUpdateExtensionsRequest; //

const { status, data } = await apiInstance.replaceWebsitePHPExtensionsV1(
    websiteUid,
    agencyHostingV1PhpUpdateExtensionsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1PhpUpdateExtensionsRequest** | **AgencyHostingV1PhpUpdateExtensionsRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


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

# **replaceWebsitePHPOptionsV1**
> CommonSuccessEmptyResource replaceWebsitePHPOptionsV1(agencyHostingV1PhpUpdateOptionsRequest)

Replaces the custom php.ini values on an Agency Plan website with the ones provided. Any option not in the request is reset to its default, so call the options endpoint first and send the full desired set. Sending an empty array resets every option to its default.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration,
    AgencyHostingV1PhpUpdateOptionsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1PhpUpdateOptionsRequest: AgencyHostingV1PhpUpdateOptionsRequest; //

const { status, data } = await apiInstance.replaceWebsitePHPOptionsV1(
    websiteUid,
    agencyHostingV1PhpUpdateOptionsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1PhpUpdateOptionsRequest** | **AgencyHostingV1PhpUpdateOptionsRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


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

# **updateWebsitePHPVersionV1**
> CommonSuccessEmptyResource updateWebsitePHPVersionV1(agencyHostingV1PhpUpdateVersionRequest)

Switches an Agency Plan website to a different PHP version. Call the available versions endpoint first to see which versions can be selected. The website restarts on the new version, so requests served during the switch may fail and code that is incompatible with the target version will break.

### Example

```typescript
import {
    AgencyHostingPHPApi,
    Configuration,
    AgencyHostingV1PhpUpdateVersionRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingPHPApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1PhpUpdateVersionRequest: AgencyHostingV1PhpUpdateVersionRequest; //

const { status, data } = await apiInstance.updateWebsitePHPVersionV1(
    websiteUid,
    agencyHostingV1PhpUpdateVersionRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1PhpUpdateVersionRequest** | **AgencyHostingV1PhpUpdateVersionRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


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

