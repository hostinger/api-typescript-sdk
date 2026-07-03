# WordPressPluginsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**activateWordPressPluginV1**](#activatewordpresspluginv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/activate | Activate WordPress plugin|
|[**checkIfWooCommerceIsInstalledV1**](#checkifwoocommerceisinstalledv1) | **GET** /api/hosting/v1/wordpress/plugins/is-woocommerce-installed | Check if WooCommerce is installed|
|[**deactivateWordPressPluginV1**](#deactivatewordpresspluginv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/deactivate | Deactivate WordPress plugin|
|[**installWordPressPluginsV1**](#installwordpresspluginsv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/install | Install WordPress plugins|
|[**listAvailableWordPressPluginsV1**](#listavailablewordpresspluginsv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/available | List available WordPress plugins|
|[**listInstalledWordPressPluginsV1**](#listinstalledwordpresspluginsv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins | List installed WordPress plugins|
|[**listSuggestedWordPressPluginsV1**](#listsuggestedwordpresspluginsv1) | **GET** /api/hosting/v1/wordpress/plugins/suggested | List suggested WordPress plugins|
|[**searchWordPressPluginsV1**](#searchwordpresspluginsv1) | **GET** /api/hosting/v1/wordpress/plugins | Search WordPress plugins|
|[**uninstallWordPressPluginsV1**](#uninstallwordpresspluginsv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/uninstall | Uninstall WordPress plugins|
|[**updateHostingerWordPressPluginV1**](#updatehostingerwordpresspluginv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/hostinger/update | Update Hostinger WordPress plugin|
|[**updateWordPressPluginsV1**](#updatewordpresspluginsv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/update | Update WordPress plugins|

# **activateWordPressPluginV1**
> CommonSuccessEmptyResource activateWordPressPluginV1(wordPressV1PluginsActivatePluginRequest)

Activate an installed plugin on a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the activation job has been queued.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration,
    WordPressV1PluginsActivatePluginRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1PluginsActivatePluginRequest: WordPressV1PluginsActivatePluginRequest; //

const { status, data } = await apiInstance.activateWordPressPluginV1(
    username,
    software,
    wordPressV1PluginsActivatePluginRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1PluginsActivatePluginRequest** | **WordPressV1PluginsActivatePluginRequest**|  | |
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

# **checkIfWooCommerceIsInstalledV1**
> WordPressV1PluginsWoocommerceInstalledResource checkIfWooCommerceIsInstalledV1()

Check whether WooCommerce is installed on any WordPress installation of a domain. Optionally filter by domain to scope the check.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let domain: string; //Filter by domain name (exact match) (optional) (default to undefined)

const { status, data } = await apiInstance.checkIfWooCommerceIsInstalledV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Filter by domain name (exact match) | (optional) defaults to undefined|


### Return type

**WordPressV1PluginsWoocommerceInstalledResource**

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

# **deactivateWordPressPluginV1**
> CommonSuccessEmptyResource deactivateWordPressPluginV1(wordPressV1PluginsDeactivatePluginRequest)

Deactivate an installed plugin on a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the deactivation job has been queued.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration,
    WordPressV1PluginsDeactivatePluginRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1PluginsDeactivatePluginRequest: WordPressV1PluginsDeactivatePluginRequest; //

const { status, data } = await apiInstance.deactivateWordPressPluginV1(
    username,
    software,
    wordPressV1PluginsDeactivatePluginRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1PluginsDeactivatePluginRequest** | **WordPressV1PluginsDeactivatePluginRequest**|  | |
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

# **installWordPressPluginsV1**
> CommonSuccessEmptyResource installWordPressPluginsV1(wordPressV1PluginsInstallPluginsRequest)

Install one or more plugins on an existing WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field). Use GET /api/hosting/v1/wordpress/plugins to discover the plugin slugs available for installation.  This operation is asynchronous: a successful response only means the install job has been queued, not that the plugins are ready.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration,
    WordPressV1PluginsInstallPluginsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1PluginsInstallPluginsRequest: WordPressV1PluginsInstallPluginsRequest; //

const { status, data } = await apiInstance.installWordPressPluginsV1(
    username,
    software,
    wordPressV1PluginsInstallPluginsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1PluginsInstallPluginsRequest** | **WordPressV1PluginsInstallPluginsRequest**|  | |
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

# **listAvailableWordPressPluginsV1**
> Array<WordPressV1PluginsAvailablePluginResource> listAvailableWordPressPluginsV1()

List plugins recommended for installation on a WordPress installation that are not yet installed.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.listAvailableWordPressPluginsV1(
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

**Array<WordPressV1PluginsAvailablePluginResource>**

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

# **listInstalledWordPressPluginsV1**
> Array<WordPressV1PluginsInstalledPluginResource> listInstalledWordPressPluginsV1()

List plugins installed on a WordPress installation, including their status, available updates and known vulnerabilities.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let category: 'cache'; //Filter installed plugins by category. (optional) (default to undefined)

const { status, data } = await apiInstance.listInstalledWordPressPluginsV1(
    username,
    software,
    category
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|
| **category** | [**&#39;cache&#39;**]**Array<&#39;cache&#39;>** | Filter installed plugins by category. | (optional) defaults to undefined|


### Return type

**Array<WordPressV1PluginsInstalledPluginResource>**

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

# **listSuggestedWordPressPluginsV1**
> Array<WordPressV1PluginsSuggestedPluginGroupResource> listSuggestedWordPressPluginsV1()

List curated plugin suggestions grouped by website type.  Use the returned `slug` values with POST /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/install.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let orderId: number; //Optionally scope suggestions to a specific order. (optional) (default to undefined)

const { status, data } = await apiInstance.listSuggestedWordPressPluginsV1(
    orderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Optionally scope suggestions to a specific order. | (optional) defaults to undefined|


### Return type

**Array<WordPressV1PluginsSuggestedPluginGroupResource>**

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

# **searchWordPressPluginsV1**
> Array<WordPressV1PluginsPluginResource> searchWordPressPluginsV1()

Search the WordPress.org plugin directory for plugins available to install.  Use the returned `slug` values with POST /api/hosting/v1/accounts/{username}/wordpress/{software}/plugins/install.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let search: string; //Search term to match against plugin names. Minimum 3 characters. (default to undefined)

const { status, data } = await apiInstance.searchWordPressPluginsV1(
    search
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **search** | [**string**] | Search term to match against plugin names. Minimum 3 characters. | defaults to undefined|


### Return type

**Array<WordPressV1PluginsPluginResource>**

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

# **uninstallWordPressPluginsV1**
> CommonSuccessEmptyResource uninstallWordPressPluginsV1(wordPressV1PluginsUninstallPluginsRequest)

Uninstall one or more plugins from a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the uninstall job has been queued.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration,
    WordPressV1PluginsUninstallPluginsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1PluginsUninstallPluginsRequest: WordPressV1PluginsUninstallPluginsRequest; //

const { status, data } = await apiInstance.uninstallWordPressPluginsV1(
    username,
    software,
    wordPressV1PluginsUninstallPluginsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1PluginsUninstallPluginsRequest** | **WordPressV1PluginsUninstallPluginsRequest**|  | |
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

# **updateHostingerWordPressPluginV1**
> CommonSuccessEmptyResource updateHostingerWordPressPluginV1(wordPressV1PluginsUpdateHostingerPluginRequest)

Update a Hostinger plugin to its latest version on a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the update job has been queued.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration,
    WordPressV1PluginsUpdateHostingerPluginRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1PluginsUpdateHostingerPluginRequest: WordPressV1PluginsUpdateHostingerPluginRequest; //

const { status, data } = await apiInstance.updateHostingerWordPressPluginV1(
    username,
    software,
    wordPressV1PluginsUpdateHostingerPluginRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1PluginsUpdateHostingerPluginRequest** | **WordPressV1PluginsUpdateHostingerPluginRequest**|  | |
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

# **updateWordPressPluginsV1**
> CommonSuccessEmptyResource updateWordPressPluginsV1(wordPressV1PluginsUpdatePluginsRequest)

Update one or more installed plugins to their latest version on a WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the update job has been queued.

### Example

```typescript
import {
    WordPressPluginsApi,
    Configuration,
    WordPressV1PluginsUpdatePluginsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressPluginsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1PluginsUpdatePluginsRequest: WordPressV1PluginsUpdatePluginsRequest; //

const { status, data } = await apiInstance.updateWordPressPluginsV1(
    username,
    software,
    wordPressV1PluginsUpdatePluginsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1PluginsUpdatePluginsRequest** | **WordPressV1PluginsUpdatePluginsRequest**|  | |
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

