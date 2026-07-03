# WordPressInstallationsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**installWordPressV1**](#installwordpressv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/installations | Install WordPress|
|[**listWordPressInstallationsV1**](#listwordpressinstallationsv1) | **GET** /api/hosting/v1/wordpress/installations | List WordPress installations|

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

