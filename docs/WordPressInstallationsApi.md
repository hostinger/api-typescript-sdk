# WordPressInstallationsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**checkIfWordPressInstallationsAreValidV1**](#checkifwordpressinstallationsarevalidv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/installations/check-is-valid | Check if WordPress installations are valid|
|[**deleteWordPressInstallationV1**](#deletewordpressinstallationv1) | **DELETE** /api/hosting/v1/accounts/{username}/wordpress/{software} | Delete WordPress installation|
|[**detectWordPressInstallationsV1**](#detectwordpressinstallationsv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/installations/detect | Detect WordPress installations|
|[**getInstallationJWTTokenV1**](#getinstallationjwttokenv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/jwt-token | Get installation JWT token|
|[**installWordPressV1**](#installwordpressv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/installations | Install WordPress|
|[**listAvailableWordPressCoreUpdatesV1**](#listavailablewordpresscoreupdatesv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/updates | List available WordPress core updates|
|[**listWordPressInstallationsV1**](#listwordpressinstallationsv1) | **GET** /api/hosting/v1/wordpress/installations | List WordPress installations|
|[**showWordPressCoreVersionV1**](#showwordpresscoreversionv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/version | Show WordPress core version|
|[**updateWordPressCoreV1**](#updatewordpresscorev1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/update | Update WordPress core|

# **checkIfWordPressInstallationsAreValidV1**
> Array<WordPressV1InstallationsCheckIsValidResultResource> checkIfWordPressInstallationsAreValidV1(wordPressV1InstallationsCheckIsValidRequest)

Check whether one or more WordPress installations are valid and working correctly. Detects broken installations caused by missing files, broken plugins, themes and similar issues.  Provide the WordPress installation (software) identifiers in the body. They can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration,
    WordPressV1InstallationsCheckIsValidRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let wordPressV1InstallationsCheckIsValidRequest: WordPressV1InstallationsCheckIsValidRequest; //

const { status, data } = await apiInstance.checkIfWordPressInstallationsAreValidV1(
    username,
    wordPressV1InstallationsCheckIsValidRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1InstallationsCheckIsValidRequest** | **WordPressV1InstallationsCheckIsValidRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|


### Return type

**Array<WordPressV1InstallationsCheckIsValidResultResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWordPressInstallationV1**
> CommonSuccessEmptyResource deleteWordPressInstallationV1(wordPressV1InstallationsDeleteInstallationRequest)

Delete the specified WordPress installation, with optional file and database removal. This removes all associated components including plugins, themes, staging websites and any other related data.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration,
    WordPressV1InstallationsDeleteInstallationRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1InstallationsDeleteInstallationRequest: WordPressV1InstallationsDeleteInstallationRequest; //

const { status, data } = await apiInstance.deleteWordPressInstallationV1(
    username,
    software,
    wordPressV1InstallationsDeleteInstallationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1InstallationsDeleteInstallationRequest** | **WordPressV1InstallationsDeleteInstallationRequest**|  | |
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

# **detectWordPressInstallationsV1**
> CommonSuccessEmptyResource detectWordPressInstallationsV1()

Trigger a background scan to detect WordPress installations for the account.  This operation is asynchronous: a successful response only means the scan has been queued. Poll GET /api/hosting/v1/wordpress/installations to fetch the detected installations once the scan completes.

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.detectWordPressInstallationsV1(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


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

# **getInstallationJWTTokenV1**
> WordPressV1InstallationsJwtTokenResource getInstallationJWTTokenV1()

Return a JWT token used to authenticate requests against the specified WordPress installation, including its MCP (Model Context Protocol) endpoint.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.getInstallationJWTTokenV1(
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

**WordPressV1InstallationsJwtTokenResource**

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

# **installWordPressV1**
> CommonSuccessEmptyResource installWordPressV1(wordPressV1InstallationsInstallWordPressRequest)

Install WordPress on an existing website.  The website must already exist before calling this endpoint. To create a new website first, use POST /api/hosting/v1/websites and poll GET /api/hosting/v1/websites until it appears.  Call GET /api/hosting/v1/wordpress/installations filtered by username and domain before proceeding to check whether WordPress is already installed on the target domain/path. If WordPress already exists and `overwrite` is false (the default), the async job will fail.  This operation is asynchronous: a successful response only means the install job has been queued, not that WordPress is ready. Installation typically takes 1-2 minutes. Poll GET /api/hosting/v1/wordpress/installations filtered by username and domain to track progress. When the installation appears in that list, WordPress is ready.

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration,
    WordPressV1InstallationsInstallWordPressRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let wordPressV1InstallationsInstallWordPressRequest: WordPressV1InstallationsInstallWordPressRequest; //

const { status, data } = await apiInstance.installWordPressV1(
    username,
    wordPressV1InstallationsInstallWordPressRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1InstallationsInstallWordPressRequest** | **WordPressV1InstallationsInstallWordPressRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|


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

# **listAvailableWordPressCoreUpdatesV1**
> Array<WordPressV1InstallationsUpdateResource> listAvailableWordPressCoreUpdatesV1()

List available WordPress core updates for the specified installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.listAvailableWordPressCoreUpdatesV1(
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

**Array<WordPressV1InstallationsUpdateResource>**

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

# **listWordPressInstallationsV1**
> Array<WordPressV1InstallationsWordPressInstallationResource> listWordPressInstallationsV1()

List WordPress installations accessible to the authenticated client.  Use this endpoint to discover existing WordPress installations and to poll for installation status after calling the install endpoint. When a newly requested installation appears in this list, WordPress is ready. Filter by username and domain to narrow results to a specific website.  Each installation includes a `valid` flag and, when invalid, a `validationError` describing why.

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; //Filter by specific username (optional) (default to undefined)
let domain: string; //Filter by domain name (exact match) (optional) (default to undefined)
let ownership: 'owned' | 'managed' | 'all'; //Filter by ownership type. Defaults to \"owned\". Use \"all\" to include both owned and managed installations. (optional) (default to undefined)

const { status, data } = await apiInstance.listWordPressInstallationsV1(
    username,
    domain,
    ownership
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] | Filter by specific username | (optional) defaults to undefined|
| **domain** | [**string**] | Filter by domain name (exact match) | (optional) defaults to undefined|
| **ownership** | [**&#39;owned&#39; | &#39;managed&#39; | &#39;all&#39;**]**Array<&#39;owned&#39; &#124; &#39;managed&#39; &#124; &#39;all&#39;>** | Filter by ownership type. Defaults to \&quot;owned\&quot;. Use \&quot;all\&quot; to include both owned and managed installations. | (optional) defaults to undefined|


### Return type

**Array<WordPressV1InstallationsWordPressInstallationResource>**

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

# **showWordPressCoreVersionV1**
> WordPressV1InstallationsVersionResource showWordPressCoreVersionV1()

Show the WordPress core version for the specified installation, along with known vulnerabilities affecting it.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.showWordPressCoreVersionV1(
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

**WordPressV1InstallationsVersionResource**

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

# **updateWordPressCoreV1**
> CommonSuccessEmptyResource updateWordPressCoreV1(wordPressV1InstallationsUpdateInstallationRequest)

Update the WordPress core for the specified installation (minor update or a specific version).  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).  This operation is asynchronous: a successful response only means the update job has been queued.

### Example

```typescript
import {
    WordPressInstallationsApi,
    Configuration,
    WordPressV1InstallationsUpdateInstallationRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressInstallationsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1InstallationsUpdateInstallationRequest: WordPressV1InstallationsUpdateInstallationRequest; //

const { status, data } = await apiInstance.updateWordPressCoreV1(
    username,
    software,
    wordPressV1InstallationsUpdateInstallationRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1InstallationsUpdateInstallationRequest** | **WordPressV1InstallationsUpdateInstallationRequest**|  | |
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

