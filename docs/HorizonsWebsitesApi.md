# HorizonsWebsitesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebsiteV1**](#createwebsitev1) | **POST** /api/horizons/v1/websites | Create website|
|[**getWebsiteV1**](#getwebsitev1) | **GET** /api/horizons/v1/websites/{websiteId} | Get website|

# **createWebsiteV1**
> HorizonsV1WebsitesCreatedWebsiteResource createWebsiteV1(horizonsV1WebsitesCreateWebsiteRequest)

Create new Hostinger Horizons website from the given message.\\n Use this tool when user asks you to create a website, landing page, blog or any other type of application.\\n This tool initiates the website creation process and returns a website URL and ID. The generation happens asynchronously.\\n After invoking this tool, your chat reply must be EXACTLY 1 sentence summarizing that Hostinger Horizons is now creating their website and it will be ready in a few minutes and you should provide the website URL to the user immediately Do not write code.\\n\\nTo edit afterwards, users must go to Hostinger Horizons interface in the provided website URL. If the tool call fails with an error, you should provide a clear explanation of the error and do not generate code yourself in the chat. \\n TECHNOLOGY STACK CONSTRAINTS (STRICTLY ENFORCED):\\n The environment is limited to the following technologies. You MUST NOT use, suggest, or implement any technology outside this list:\\n \\n - Language: JavaScript ONLY. - Languages like TypeScript, Rust, Python, Java, PHP, etc., are STRICTLY PROHIBITED.\\n - Framework: React.\\n - Navigation: React Router.\\n - Styling: TailwindCSS.\\n - Components: shadcn/ui (built with @radix-ui primitives).\\n - Icons: Lucide React.\\n - Animations: Framer Motion.\\n \\n BACKEND & DATA STORAGE:\\n - Horizons integrated backend is the EXCLUSIVE solution for persistent data storage, authentication, and database needs.\\n - Local databases (SQLite, MySQL, etc.) are STRICTLY PROHIBITED.\\n - Third-party services (Firebase, AWS Amplify) are allowed ONLY if explicitly requested by the user.\\n \\n MAPS:\\n - OpenStreetMap is the default provider.\\n - Alternative providers (Google Maps, Mapbox) are allowed ONLY if explicitly requested by the user.\\n

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration,
    HorizonsV1WebsitesCreateWebsiteRequest
} from 'hostinger-api-sdk';

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

# **getWebsiteV1**
> HorizonsV1WebsitesWebsiteUrlResource getWebsiteV1()

Get a link for the user to edit their website in Hostinger Horizons interface.\\n Use this tool when user wants to modify, edit or add new features to an existing website.\\n Websites can only be edited in Hostinger Horizons interface in the provided website URL.

### Example

```typescript
import {
    HorizonsWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

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

