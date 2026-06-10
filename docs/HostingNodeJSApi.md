# HostingNodeJSApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createNodeJSBuildFromArchiveV1**](#createnodejsbuildfromarchivev1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/from-archive | Create NodeJS build from archive|
|[**getNodeJSBuildLogsV1**](#getnodejsbuildlogsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/{uuid}/logs | Get NodeJS build logs|
|[**listNodeJSBuildsV1**](#listnodejsbuildsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds | List NodeJS builds|

# **createNodeJSBuildFromArchiveV1**
> HostingV1NodeJsBuildResource createNodeJSBuildFromArchiveV1(hostingV1NodeJsCreateFromArchiveRequest)

Upload a project archive, auto-detect build settings, and immediately start a Node.js build.  This is the recommended single-step approach for deploying a Node.js application. The archive is uploaded to the website\'s file storage, build settings are auto-detected from the package.json inside the archive, and the build process starts automatically. Optional override fields take precedence over auto-detected values. Maximum archive size is 50MB.  Before archiving, exclude `node_modules/` and any build output directories (e.g. `dist/`, `.next/`, `build/`) — they are not needed because the build process runs the install step automatically, and including them unnecessarily increases the archive size. This also helps keep the archive well under the 50MB limit.  Example (zip): ``` zip -r archive.zip . --exclude \"node_modules/_*\" --exclude \"dist/_*\" ```  The returned build `uuid` can be used to poll progress and retrieve logs via the `Get Node.js Build Logs` endpoint.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration,
    HostingV1NodeJsCreateFromArchiveRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1NodeJsCreateFromArchiveRequest: HostingV1NodeJsCreateFromArchiveRequest; //

const { status, data } = await apiInstance.createNodeJSBuildFromArchiveV1(
    username,
    domain,
    hostingV1NodeJsCreateFromArchiveRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1NodeJsCreateFromArchiveRequest** | **HostingV1NodeJsCreateFromArchiveRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1NodeJsBuildResource**

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

# **getNodeJSBuildLogsV1**
> HostingV1NodeJsBuildLogsResource getNodeJSBuildLogsV1()

Retrieve logs from a specific Node.js build process.  To stream live output while a build is running, poll this endpoint repeatedly while the build state is `running`, passing the previously returned `lines` count as `from_line` to fetch only new output since the last call. Log content may contain ANSI escape sequences (color codes).

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let uuid: string; //Build UUID (default to undefined)
let fromLine: number; //Line from which to start retrieving logs (optional) (default to 0)

const { status, data } = await apiInstance.getNodeJSBuildLogsV1(
    username,
    domain,
    uuid,
    fromLine
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **uuid** | [**string**] | Build UUID | defaults to undefined|
| **fromLine** | [**number**] | Line from which to start retrieving logs | (optional) defaults to 0|


### Return type

**HostingV1NodeJsBuildLogsResource**

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
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listNodeJSBuildsV1**
> HostingListNodeJSBuildsV1200Response listNodeJSBuildsV1()

Retrieve a paginated list of Node.js build processes for a specific website.  Each build represents a single run of the Node.js build pipeline. Use the `states` query parameter to filter results by build state (pending, running, completed, failed). Use the `uuid` from a build to poll its output via the `Get Node.js Build Logs` endpoint.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let states: Array<'pending' | 'running' | 'completed' | 'failed'>; //Build states to filter by (optional) (default to undefined)

const { status, data } = await apiInstance.listNodeJSBuildsV1(
    username,
    domain,
    page,
    perPage,
    states
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **states** | **Array<&#39;pending&#39; &#124; &#39;running&#39; &#124; &#39;completed&#39; &#124; &#39;failed&#39;>** | Build states to filter by | (optional) defaults to undefined|


### Return type

**HostingListNodeJSBuildsV1200Response**

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

