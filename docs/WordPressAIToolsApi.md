# WordPressAIToolsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**setAIOptionStatusV1**](#setaioptionstatusv1) | **PATCH** /api/hosting/v1/accounts/{username}/wordpress/{software}/hostinger-plugins/ai-option/status | Set AI option status|
|[**showAIOptionStatusV1**](#showaioptionstatusv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/hostinger-plugins/ai-option/status | Show AI option status|

# **setAIOptionStatusV1**
> CommonSuccessEmptyResource setAIOptionStatusV1(wordPressV1HostingerPluginsUpdateAiOptionStatusRequest)

Enable or disable an AI option for the Hostinger Tools plugin on the specified WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressAIToolsApi,
    Configuration,
    WordPressV1HostingerPluginsUpdateAiOptionStatusRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressAIToolsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1HostingerPluginsUpdateAiOptionStatusRequest: WordPressV1HostingerPluginsUpdateAiOptionStatusRequest; //

const { status, data } = await apiInstance.setAIOptionStatusV1(
    username,
    software,
    wordPressV1HostingerPluginsUpdateAiOptionStatusRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1HostingerPluginsUpdateAiOptionStatusRequest** | **WordPressV1HostingerPluginsUpdateAiOptionStatusRequest**|  | |
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

# **showAIOptionStatusV1**
> WordPressV1HostingerPluginsAiOptionStatusResource showAIOptionStatusV1()

Show the current AI option status for the Hostinger Tools plugin on the specified WordPress installation. Filter by `option` to return a single option, or omit it to return all options.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressAIToolsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressAIToolsApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let option: 'llmstxt' | 'web2agent'; //Filter the status by a single AI option. (optional) (default to undefined)

const { status, data } = await apiInstance.showAIOptionStatusV1(
    username,
    software,
    option
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|
| **option** | [**&#39;llmstxt&#39; | &#39;web2agent&#39;**]**Array<&#39;llmstxt&#39; &#124; &#39;web2agent&#39;>** | Filter the status by a single AI option. | (optional) defaults to undefined|


### Return type

**WordPressV1HostingerPluginsAiOptionStatusResource**

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

