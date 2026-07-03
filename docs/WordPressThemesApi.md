# WordPressThemesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**activateWordPressThemeV1**](#activatewordpressthemev1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/themes/activate | Activate WordPress theme|
|[**installWordPressThemeV1**](#installwordpressthemev1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/themes/install | Install WordPress theme|
|[**listInstalledWordPressThemesV1**](#listinstalledwordpressthemesv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/themes | List installed WordPress themes|
|[**listWordPressThemesV1**](#listwordpressthemesv1) | **GET** /api/hosting/v1/wordpress/themes | List WordPress themes|
|[**uninstallWordPressThemesV1**](#uninstallwordpressthemesv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/themes/uninstall | Uninstall WordPress themes|
|[**updateWordPressThemesV1**](#updatewordpressthemesv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/themes/update | Update WordPress themes|

# **activateWordPressThemeV1**
> CommonSuccessEmptyResource activateWordPressThemeV1(wordPressV1ThemesActivateThemeRequest)

Activate an installed theme on a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the activation job has been queued.

### Example

```typescript
import {
    WordPressThemesApi,
    Configuration,
    WordPressV1ThemesActivateThemeRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressThemesApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1ThemesActivateThemeRequest: WordPressV1ThemesActivateThemeRequest; //

const { status, data } = await apiInstance.activateWordPressThemeV1(
    username,
    software,
    wordPressV1ThemesActivateThemeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1ThemesActivateThemeRequest** | **WordPressV1ThemesActivateThemeRequest**|  | |
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

# **installWordPressThemeV1**
> CommonSuccessEmptyResource installWordPressThemeV1(wordPressV1ThemesInstallThemeRequest)

Install a theme on an existing WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  When the theme is one of the Hostinger themes (hostinger-blog, hostinger-affiliate-theme, hostinger-ai-theme), the optional `palette`, `layout`, and `font` fields are forwarded to the custom installer (defaults: palette1, layout1, default). For any other theme they are ignored.  This operation is asynchronous: a successful response only means the install job has been queued, not that the theme is ready.

### Example

```typescript
import {
    WordPressThemesApi,
    Configuration,
    WordPressV1ThemesInstallThemeRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressThemesApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1ThemesInstallThemeRequest: WordPressV1ThemesInstallThemeRequest; //

const { status, data } = await apiInstance.installWordPressThemeV1(
    username,
    software,
    wordPressV1ThemesInstallThemeRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1ThemesInstallThemeRequest** | **WordPressV1ThemesInstallThemeRequest**|  | |
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

# **listInstalledWordPressThemesV1**
> Array<WordPressV1ThemesInstalledThemeResource> listInstalledWordPressThemesV1()

List themes installed on a WordPress installation, including their status, available updates and known vulnerabilities.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressThemesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressThemesApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.listInstalledWordPressThemesV1(
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

**Array<WordPressV1ThemesInstalledThemeResource>**

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

# **listWordPressThemesV1**
> Array<WordPressV1ThemesThemeResource> listWordPressThemesV1()

List WordPress themes available to install.  Use the returned `slug` values with POST /api/hosting/v1/accounts/{username}/wordpress/{software}/themes/install.

### Example

```typescript
import {
    WordPressThemesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressThemesApi(configuration);

let orderId: number; //Optionally scope themes to a specific order. (optional) (default to undefined)
let search: string; //Search term to match against theme names. (optional) (default to undefined)

const { status, data } = await apiInstance.listWordPressThemesV1(
    orderId,
    search
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Optionally scope themes to a specific order. | (optional) defaults to undefined|
| **search** | [**string**] | Search term to match against theme names. | (optional) defaults to undefined|


### Return type

**Array<WordPressV1ThemesThemeResource>**

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

# **uninstallWordPressThemesV1**
> CommonSuccessEmptyResource uninstallWordPressThemesV1(wordPressV1ThemesUninstallThemesRequest)

Uninstall one or more themes from a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the uninstall job has been queued.

### Example

```typescript
import {
    WordPressThemesApi,
    Configuration,
    WordPressV1ThemesUninstallThemesRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressThemesApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1ThemesUninstallThemesRequest: WordPressV1ThemesUninstallThemesRequest; //

const { status, data } = await apiInstance.uninstallWordPressThemesV1(
    username,
    software,
    wordPressV1ThemesUninstallThemesRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1ThemesUninstallThemesRequest** | **WordPressV1ThemesUninstallThemesRequest**|  | |
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

# **updateWordPressThemesV1**
> CommonSuccessEmptyResource updateWordPressThemesV1(wordPressV1ThemesUpdateThemesRequest)

Update one or more installed themes to their latest version on a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the update job has been queued.

### Example

```typescript
import {
    WordPressThemesApi,
    Configuration,
    WordPressV1ThemesUpdateThemesRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressThemesApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1ThemesUpdateThemesRequest: WordPressV1ThemesUpdateThemesRequest; //

const { status, data } = await apiInstance.updateWordPressThemesV1(
    username,
    software,
    wordPressV1ThemesUpdateThemesRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1ThemesUpdateThemesRequest** | **WordPressV1ThemesUpdateThemesRequest**|  | |
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

