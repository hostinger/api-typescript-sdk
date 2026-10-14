# WordPressAIContentApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**generateImagesV1**](#generateimagesv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/content/images/generate | Generate images|

# **generateImagesV1**
> WordPressV1ContentGeneratedImagesResource generateImagesV1(wordPressV1ContentGenerateImagesRequest)

Generate one or more images from a prompt and an image type for the specified WordPress installation. Images are returned inline as base64-encoded PNGs. They match the requested aspect ratio and are never smaller than the requested size; logos are transparent PNGs cropped to the mark.  Generation is synchronous and can take up to a minute. The endpoint is limited to 10 requests per minute.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressAIContentApi,
    Configuration,
    WordPressV1ContentGenerateImagesRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new WordPressAIContentApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1ContentGenerateImagesRequest: WordPressV1ContentGenerateImagesRequest; //

const { status, data } = await apiInstance.generateImagesV1(
    username,
    software,
    wordPressV1ContentGenerateImagesRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1ContentGenerateImagesRequest** | **WordPressV1ContentGenerateImagesRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|


### Return type

**WordPressV1ContentGeneratedImagesResource**

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

