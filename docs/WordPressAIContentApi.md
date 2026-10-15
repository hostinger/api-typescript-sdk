# WordPressAIContentApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**generateImagesV1**](#generateimagesv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/content/images/generate | Generate images|
|[**getGenerationResultV1**](#getgenerationresultv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/content/generations/{generation_id} | Get generation result|

# **generateImagesV1**
> WordPressV1ContentGenerationResource generateImagesV1(wordPressV1ContentGenerateImagesRequest)

Start generating one or more images from a prompt and an image type for the specified WordPress installation. The generation runs asynchronously: the response is returned right away with `status: in-progress` and a `generation_id`. Poll GET /api/hosting/v1/accounts/{username}/wordpress/{software}/content/generations/{generation_id} every few seconds until `status` is `completed` or `failed`.  A completed generation returns temporary image URLs together with the time they expire; download the images before then. Images match the requested aspect ratio and are never smaller than the requested size; logos are transparent images cropped to the mark.  Only one image generation can run per installation at a time: while one is still in progress the endpoint returns 409 without the ID of the running generation, so a caller that did not receive the `202` has to wait for it to finish (up to a few minutes) before starting a new one. The endpoint is limited to 10 requests per minute.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

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

**WordPressV1ContentGenerationResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**202** | Accepted response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**409** | Conflict response. &#x60;Retry-After&#x60;, when present, is the number of seconds to wait before retrying. |  * Retry-After - Seconds to wait before retrying the request <br>  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getGenerationResultV1**
> WordPressV1ContentGenerationResource getGenerationResultV1()

Get the result of an AI content generation started for the specified WordPress installation, such as an image generation started with POST /api/hosting/v1/accounts/{username}/wordpress/{software}/content/images/generate.  While the generation is still running only `status: in-progress` is returned; poll every few seconds. Once `completed`, `result` holds the generated content shaped according to `type`: temporary image URLs together with the time they expire for `image-generation`, or the generated website document for `website-generation` (started from the Hostinger WordPress plugin). A `failed` generation has no `result`. Unknown or expired generation IDs return 404.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressAIContentApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new WordPressAIContentApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let generationId: string; //Generation ID returned when the generation was started (default to undefined)
let type: 'website-generation' | 'image-generation'; //Generation type to look up. When omitted, every generation type is checked. (optional) (default to undefined)

const { status, data } = await apiInstance.getGenerationResultV1(
    username,
    software,
    generationId,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|
| **generationId** | [**string**] | Generation ID returned when the generation was started | defaults to undefined|
| **type** | [**&#39;website-generation&#39; | &#39;image-generation&#39;**]**Array<&#39;website-generation&#39; &#124; &#39;image-generation&#39;>** | Generation type to look up. When omitted, every generation type is checked. | (optional) defaults to undefined|


### Return type

**WordPressV1ContentGenerationResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

