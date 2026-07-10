# AgencyHostingWebsitesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**buildAgencyPlanWebsiteNodeJSAssetsV1**](#buildagencyplanwebsitenodejsassetsv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/build-assets | Build Agency Plan website NodeJS assets|
|[**deleteAgencyPlanWebsiteV1**](#deleteagencyplanwebsitev1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid} | Delete Agency Plan website|
|[**getAgencyPlanWebsiteDetailsV1**](#getagencyplanwebsitedetailsv1) | **GET** /api/agency-hosting/v1/websites/{website_uid} | Get Agency Plan website details|
|[**listRunningAgencyPlanWebsiteProcessesV1**](#listrunningagencyplanwebsiteprocessesv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/processes | List running Agency Plan website processes|

# **buildAgencyPlanWebsiteNodeJSAssetsV1**
> CommonSuccessEmptyResource buildAgencyPlanWebsiteNodeJSAssetsV1(agencyHostingV1WebsitesBuildAssetsRequest)

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

const { status, data } = await apiInstance.buildAgencyPlanWebsiteNodeJSAssetsV1(
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

# **deleteAgencyPlanWebsiteV1**
> AgencyHostingV1WebsitesWebsiteDeletionResource deleteAgencyPlanWebsiteV1()

Deletes an Agency Plan website and schedules cleanup of its resources.  This action is irreversible. Website files, databases, and linked domains are removed.

### Example

```typescript
import {
    AgencyHostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsitesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.deleteAgencyPlanWebsiteV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**AgencyHostingV1WebsitesWebsiteDeletionResource**

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

# **getAgencyPlanWebsiteDetailsV1**
> AgencyHostingV1WebsitesWebsiteResource getAgencyPlanWebsiteDetailsV1()

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

const { status, data } = await apiInstance.getAgencyPlanWebsiteDetailsV1(
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

# **listRunningAgencyPlanWebsiteProcessesV1**
> Array<AgencyHostingV1WebsitesWebsiteProcessResource> listRunningAgencyPlanWebsiteProcessesV1()

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

const { status, data } = await apiInstance.listRunningAgencyPlanWebsiteProcessesV1(
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

