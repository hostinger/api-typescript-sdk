# AgencyHostingWebsitesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**buildWebsiteNodeJSAssetsV1**](#buildwebsitenodejsassetsv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/build-assets | Build website NodeJS assets|
|[**deleteWebsiteV1**](#deletewebsitev1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid} | Delete website|
|[**getWebsiteDetailsV1**](#getwebsitedetailsv1) | **GET** /api/agency-hosting/v1/websites/{website_uid} | Get website details|
|[**listWebsiteProcessesV1**](#listwebsiteprocessesv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/processes | List website processes|

# **buildWebsiteNodeJSAssetsV1**
> CommonSuccessEmptyResource buildWebsiteNodeJSAssetsV1(agencyHostingV1WebsitesBuildAssetsRequest)

Builds and deploys a Node.js application for an Agency Plan website from an already-uploaded archive.  Upload the archive to file browser first, then provide its relative path from document root in this request. Website contents are overwritten by the build result, which is deployed to public_html.

### Example

```typescript
import {
    AgencyHostingWebsitesApi,
    Configuration,
    AgencyHostingV1WebsitesBuildAssetsRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsitesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1WebsitesBuildAssetsRequest: AgencyHostingV1WebsitesBuildAssetsRequest; //

const { status, data } = await apiInstance.buildWebsiteNodeJSAssetsV1(
    websiteUid,
    agencyHostingV1WebsitesBuildAssetsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1WebsitesBuildAssetsRequest** | **AgencyHostingV1WebsitesBuildAssetsRequest**|  | |
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

# **deleteWebsiteV1**
> CommonSuccessEmptyResource deleteWebsiteV1()

Permanently deletes an Agency Plan website. Deletion is processed asynchronously: the website is immediately transitioned to a deleting state and the underlying server resources are removed in the background.

### Example

```typescript
import {
    AgencyHostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsitesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.deleteWebsiteV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


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

# **getWebsiteDetailsV1**
> AgencyHostingV1WebsitesWebsiteResource getWebsiteDetailsV1()

Retrieves detailed information about a specific Agency Plan website, including configuration, status, metadata, hosting plan details, and resource quotas.

### Example

```typescript
import {
    AgencyHostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsitesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.getWebsiteDetailsV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**AgencyHostingV1WebsitesWebsiteResource**

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

# **listWebsiteProcessesV1**
> Array<AgencyHostingV1WebsitesWebsiteProcessResource> listWebsiteProcessesV1()

Lists active and recently completed asynchronous processes for an Agency Plan website.  Each process has a unique ID (for tracking), a type, and a status (running, completed, failed). Poll this endpoint after initiating async operations (SSL setup, backups, cloning) to track progress.

### Example

```typescript
import {
    AgencyHostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsitesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.listWebsiteProcessesV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**Array<AgencyHostingV1WebsitesWebsiteProcessResource>**

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

