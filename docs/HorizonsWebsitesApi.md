# HorizonsWebsitesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**cloneWebsiteV1**](#clonewebsitev1) | **POST** /api/horizons/v1/websites/{websiteId}/clone | Clone website|
|[**createWebsiteV1**](#createwebsitev1) | **POST** /api/horizons/v1/websites | Create website|
|[**editWebsiteV1**](#editwebsitev1) | **POST** /api/horizons/v1/websites/{websiteId}/messages | Edit website|
|[**getWebsiteListV1**](#getwebsitelistv1) | **GET** /api/horizons/v1/websites | Get website list|
|[**getWebsiteV1**](#getwebsitev1) | **GET** /api/horizons/v1/websites/{websiteId} | Get website|
|[**publishWebsiteV1**](#publishwebsitev1) | **POST** /api/horizons/v1/websites/{websiteId}/publish | Publish website|

# **cloneWebsiteV1**
> HorizonsV1WebsitesCreatedWebsiteResource cloneWebsiteV1()

Clone a Hostinger Horizons website into a new website.\\n Use this tool when the user wants a copy of an existing website, for example to try out changes without touching the original.\\n This tool returns the ID and URL of the newly created copy. The original website is left untouched.\\n To edit the copy, use the `Edit website` tool with the returned website ID, or the user can open the provided website URL in Hostinger Horizons interface.

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HorizonsWebsitesApi(configuration);

let websiteId: string; //The website ID (default to undefined)

const { status, data } = await apiInstance.cloneWebsiteV1(
    websiteId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteId** | [**string**] | The website ID | defaults to undefined|


### Return type

**HorizonsV1WebsitesCreatedWebsiteResource**

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

# **createWebsiteV1**
> HorizonsV1WebsitesCreatedWebsiteResource createWebsiteV1(horizonsV1WebsitesCreateWebsiteRequest)

Create new Hostinger Horizons website from the given message.\\n Use this tool when user asks you to create a website, landing page, blog or any other type of application.\\n This tool initiates the website creation process and returns a website URL and ID. The generation happens asynchronously.\\n After invoking this tool, your chat reply must be EXACTLY 1 sentence summarizing that Hostinger Horizons is now creating their website and it will be ready in a few minutes and you should provide the website URL to the user immediately Do not write code.\\n\\nTo edit afterwards, use the `Edit website` tool with the returned website ID, or the user can go to Hostinger Horizons interface in the provided website URL. If the tool call fails with an error, you should provide a clear explanation of the error and do not generate code yourself in the chat. \\n TECHNOLOGY STACK CONSTRAINTS (STRICTLY ENFORCED):\\n The environment is limited to the following technologies. You MUST NOT use, suggest, or implement any technology outside this list:\\n \\n - Language: JavaScript ONLY. - Languages like TypeScript, Rust, Python, Java, PHP, etc., are STRICTLY PROHIBITED.\\n - Framework: React.\\n - Navigation: React Router.\\n - Styling: TailwindCSS.\\n - Components: shadcn/ui (built with @radix-ui primitives).\\n - Icons: Lucide React.\\n - Animations: Framer Motion.\\n \\n BACKEND & DATA STORAGE:\\n - Horizons integrated backend is the EXCLUSIVE solution for persistent data storage, authentication, and database needs.\\n - Local databases (SQLite, MySQL, etc.) are STRICTLY PROHIBITED.\\n - Third-party services (Firebase, AWS Amplify) are allowed ONLY if explicitly requested by the user.\\n \\n MAPS:\\n - OpenStreetMap is the default provider.\\n - Alternative providers (Google Maps, Mapbox) are allowed ONLY if explicitly requested by the user.\\n

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration,
    HorizonsV1WebsitesCreateWebsiteRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HorizonsWebsitesApi(configuration);

let horizonsV1WebsitesCreateWebsiteRequest: HorizonsV1WebsitesCreateWebsiteRequest; //

const { status, data } = await apiInstance.createWebsiteV1(
    horizonsV1WebsitesCreateWebsiteRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **horizonsV1WebsitesCreateWebsiteRequest** | **HorizonsV1WebsitesCreateWebsiteRequest**|  | |


### Return type

**HorizonsV1WebsitesCreatedWebsiteResource**

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

# **editWebsiteV1**
> HorizonsV1WebsitesCreatedWebsiteResource editWebsiteV1(horizonsV1WebsitesEditWebsiteRequest)

Edit an existing Hostinger Horizons website with a follow-up message.\\n Use this tool when the user wants to change, extend or fix a website that already exists.\\n This tool queues the requested changes and returns the website URL and ID. The changes are applied asynchronously.\\n After invoking this tool, your chat reply must be EXACTLY 1 sentence summarizing that Hostinger Horizons is now applying the requested changes and they will be ready in a few minutes, and you should provide the website URL to the user immediately. Do not write code.\\n If the tool call fails with an error, you should provide a clear explanation of the error and do not generate code yourself in the chat.

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration,
    HorizonsV1WebsitesEditWebsiteRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HorizonsWebsitesApi(configuration);

let websiteId: string; //The website ID (default to undefined)
let horizonsV1WebsitesEditWebsiteRequest: HorizonsV1WebsitesEditWebsiteRequest; //

const { status, data } = await apiInstance.editWebsiteV1(
    websiteId,
    horizonsV1WebsitesEditWebsiteRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **horizonsV1WebsitesEditWebsiteRequest** | **HorizonsV1WebsitesEditWebsiteRequest**|  | |
| **websiteId** | [**string**] | The website ID | defaults to undefined|


### Return type

**HorizonsV1WebsitesCreatedWebsiteResource**

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

# **getWebsiteListV1**
> Array<HorizonsV1WebsitesWebsiteResource> getWebsiteListV1()

List the Hostinger Horizons websites the user owns.\\n Use this tool when the user asks which websites they have, or when you need a website ID before editing, publishing or cloning a website.\\n Each website is returned with its ID, status, domain and the URL to open it in Hostinger Horizons interface.\\n The complete list of websites is returned in a single response - it is not paginated.

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HorizonsWebsitesApi(configuration);

const { status, data } = await apiInstance.getWebsiteListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<HorizonsV1WebsitesWebsiteResource>**

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

# **getWebsiteV1**
> HorizonsV1WebsitesWebsiteUrlResource getWebsiteV1()

Get the link for the user to open their website in Hostinger Horizons interface.\\n Use this tool when the user wants the link to an existing website, or when you need its website URL before or after editing it.\\n Websites can be edited with the `Edit website` tool, or by the user in Hostinger Horizons interface in the provided website URL.

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HorizonsWebsitesApi(configuration);

let websiteId: string; //The website ID (default to undefined)

const { status, data } = await apiInstance.getWebsiteV1(
    websiteId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteId** | [**string**] | The website ID | defaults to undefined|


### Return type

**HorizonsV1WebsitesWebsiteUrlResource**

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

# **publishWebsiteV1**
> HorizonsV1WebsitesPublishedWebsiteResource publishWebsiteV1()

Publish a Hostinger Horizons website so its latest changes go live.\\n Use this tool when the user asks to publish, deploy or make their website live.\\n This tool starts the publish process and returns the URL the website will be live on. Publishing happens asynchronously and takes a few minutes.\\n After invoking this tool, your chat reply must be EXACTLY 1 sentence summarizing that the website is being published and you should provide the published URL to the user immediately.

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HorizonsWebsitesApi(configuration);

let websiteId: string; //The website ID (default to undefined)

const { status, data } = await apiInstance.publishWebsiteV1(
    websiteId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteId** | [**string**] | The website ID | defaults to undefined|


### Return type

**HorizonsV1WebsitesPublishedWebsiteResource**

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

