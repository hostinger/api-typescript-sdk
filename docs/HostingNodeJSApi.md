# HostingNodeJSApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**analyseFailedNodeJsBuildV1**](#analysefailednodejsbuildv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/{uuid}/analysis | Analyse failed Node.js build|
|[**clearNodeJsRuntimeLogsV1**](#clearnodejsruntimelogsv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/runtime-logs | Clear Node.js runtime logs|
|[**getNodeJSBuildLogsV1**](#getnodejsbuildlogsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/{uuid}/logs | Get NodeJS build logs|
|[**getNodeJsBuildDetailsV1**](#getnodejsbuilddetailsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/{uuid} | Get Node.js build details|
|[**getNodeJsBuildSettingsFromArchiveV1**](#getnodejsbuildsettingsfromarchivev1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/settings/from-archive | Get Node.js build settings from archive|
|[**getNodeJsBuildSettingsV1**](#getnodejsbuildsettingsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/settings | Get Node.js build settings|
|[**getNodeJsRuntimeLogsV1**](#getnodejsruntimelogsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/runtime-logs | Get Node.js runtime logs|
|[**listNodeJSBuildsV1**](#listnodejsbuildsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds | List NodeJS builds|
|[**listNodeJsEnvironmentVariablesV1**](#listnodejsenvironmentvariablesv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/settings/env | List Node.js environment variables|
|[**listNodeJsVulnerabilitiesV1**](#listnodejsvulnerabilitiesv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/vulnerabilities | List Node.js vulnerabilities|
|[**patchNodeJsVulnerabilitiesV1**](#patchnodejsvulnerabilitiesv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/vulnerabilities/patch | Patch Node.js vulnerabilities|
|[**replaceNodeJsEnvironmentVariablesV1**](#replacenodejsenvironmentvariablesv1) | **PUT** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/settings/env | Replace Node.js environment variables|
|[**restartNodeJsApplicationV1**](#restartnodejsapplicationv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/server/restart | Restart Node.js application|
|[**startNodeJsBuildV1**](#startnodejsbuildv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds | Start Node.js build|
|[**updateNodeJsBuildSettingsV1**](#updatenodejsbuildsettingsv1) | **PUT** /api/hosting/v1/accounts/{username}/websites/{domain}/nodejs/builds/settings | Update Node.js build settings|

# **analyseFailedNodeJsBuildV1**
> HostingV1NodeJsBuildAnalysisResource analyseFailedNodeJsBuildV1()

Returns an AI analysis of why a build failed and how to fix it, based on the build logs, the project file list and package.json. Only builds in the `failed` state can be analysed; any other state returns 422. When no analysis could be produced both `analysis` and `solution` are null, in which case read `Get NodeJS build logs` instead.  Each call runs the analysis again, so call it once per failed build and keep the result. Limited to 5 calls per minute per API client (429 above that).

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let uuid: string; //Build UUID (default to undefined)

const { status, data } = await apiInstance.analyseFailedNodeJsBuildV1(
    username,
    domain,
    uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **uuid** | [**string**] | Build UUID | defaults to undefined|


### Return type

**HostingV1NodeJsBuildAnalysisResource**

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

# **clearNodeJsRuntimeLogsV1**
> CommonSuccessEmptyResource clearNodeJsRuntimeLogsV1()

Empties the Node.js application\'s runtime log file. This cannot be undone, so confirm with the user before calling it. Returns success even when no log file exists yet.  Use it before reproducing a problem so the next `Get Node.js runtime logs` call returns only fresh entries; start that call with `period` again instead of reusing a `from_line` from before the clear.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.clearNodeJsRuntimeLogsV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **getNodeJSBuildLogsV1**
> HostingV1NodeJsBuildLogsResource getNodeJSBuildLogsV1()

Retrieve logs from a specific Node.js build process.  To stream live output while a build is running, poll this endpoint repeatedly while the build state is `running`, passing the previously returned `lines` count as `from_line` to fetch only new output since the last call. Log content may contain ANSI escape sequences (color codes).

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

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

# **getNodeJsBuildDetailsV1**
> HostingV1NodeJsBuildResource getNodeJsBuildDetailsV1()

Returns one build by UUID: its state (`pending`, `running`, `completed`, `failed`), the options it ran with and timestamps. Poll this while a build is pending or running. When it is failed, read `Get NodeJS build logs` and `Analyse failed Node.js build` for the cause. Returns 404 when the UUID does not belong to a build of this website.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let uuid: string; //Build UUID (default to undefined)

const { status, data } = await apiInstance.getNodeJsBuildDetailsV1(
    username,
    domain,
    uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **uuid** | [**string**] | Build UUID | defaults to undefined|


### Return type

**HostingV1NodeJsBuildResource**

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

# **getNodeJsBuildSettingsFromArchiveV1**
> HostingV1NodeJsBuildSettingsResource getNodeJsBuildSettingsFromArchiveV1()

Auto-detect Node.js build settings from a package.json inside an archive already on the server.  Use this before calling `Start Node.js Build` to preview what settings will be used, or to let the user review and override values (framework, node version, root directory, output directory, build script) before committing to a build.  The archive must already be present on the website\'s file storage. Use the `Generate Upload URL` endpoint to obtain credentials and upload the archive first.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let archivePath: string; //The path to the archive file relative to the document root of the vhost (default to undefined)

const { status, data } = await apiInstance.getNodeJsBuildSettingsFromArchiveV1(
    username,
    domain,
    archivePath
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **archivePath** | [**string**] | The path to the archive file relative to the document root of the vhost | defaults to undefined|


### Return type

**HostingV1NodeJsBuildSettingsResource**

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

# **getNodeJsBuildSettingsV1**
> HostingV1NodeJsStoredBuildSettingsResource getNodeJsBuildSettingsV1()

Returns the build settings stored for the website: framework (`app_type`), Node.js version, root and output directory, build script, entry file and package manager. Stored settings drive Git auto-deployment builds. A build started through the API uses the values sent in that request and saves them here only when no settings exist yet.  Returns 404 until the first build or the first settings update stores them. Use this after a failed build to check whether the framework or the entry file were detected wrong, then fix them with the `Update Node.js build settings` endpoint.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getNodeJsBuildSettingsV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1NodeJsStoredBuildSettingsResource**

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

# **getNodeJsRuntimeLogsV1**
> HostingV1NodeJsRuntimeLogsResource getNodeJsRuntimeLogsV1()

Returns the Node.js application\'s runtime console log entries, oldest first, each with timestamp, level and message. On the first call send `period` (`1h`, `1d`, `1w` or `1m`) and optionally `levels` and `limit` (1-5000, default 1000); when more entries match than `limit`, the newest are kept.  To poll for new entries send `total_lines + 1` from the previous response as `from_line` and omit `period`; `period` and `from_line` cannot be combined. Lines that are not JSON with a timestamp, level and message are skipped, so `logs` may hold fewer than `limit` entries while `total_lines` counts every raw line. Entries with a timestamp before `last_deployed_at` belong to the previous deployment. Returns an empty `logs` list when the application has not written a log file yet.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let period: '1h' | '1d' | '1w' | '1m'; //Time window for the first fetch. Required when `from_line` is not sent. (optional) (default to undefined)
let fromLine: number; //1-based line of the log file to start from. For polling send `total_lines + 1` from the previous response. Cannot be combined with `period`. (optional) (default to undefined)
let limit: number; //Maximum number of log entries to return. When more entries match, the newest are kept. (optional) (default to 1000)
let levels: Array<'LOG' | 'ERROR' | 'WARN' | 'INFO' | 'DEBUG' | 'TRACE'>; //Return only entries with these log levels, sent as a comma-separated list, e.g. ERROR,WARN. Matching runs on the raw log line, so entries written with numeric levels (for example by pino) are excluded while this filter is set. (optional) (default to undefined)

const { status, data } = await apiInstance.getNodeJsRuntimeLogsV1(
    username,
    domain,
    period,
    fromLine,
    limit,
    levels
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **period** | [**&#39;1h&#39; | &#39;1d&#39; | &#39;1w&#39; | &#39;1m&#39;**]**Array<&#39;1h&#39; &#124; &#39;1d&#39; &#124; &#39;1w&#39; &#124; &#39;1m&#39;>** | Time window for the first fetch. Required when &#x60;from_line&#x60; is not sent. | (optional) defaults to undefined|
| **fromLine** | [**number**] | 1-based line of the log file to start from. For polling send &#x60;total_lines + 1&#x60; from the previous response. Cannot be combined with &#x60;period&#x60;. | (optional) defaults to undefined|
| **limit** | [**number**] | Maximum number of log entries to return. When more entries match, the newest are kept. | (optional) defaults to 1000|
| **levels** | **Array<&#39;LOG&#39; &#124; &#39;ERROR&#39; &#124; &#39;WARN&#39; &#124; &#39;INFO&#39; &#124; &#39;DEBUG&#39; &#124; &#39;TRACE&#39;>** | Return only entries with these log levels, sent as a comma-separated list, e.g. ERROR,WARN. Matching runs on the raw log line, so entries written with numeric levels (for example by pino) are excluded while this filter is set. | (optional) defaults to undefined|


### Return type

**HostingV1NodeJsRuntimeLogsResource**

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
} from '@hostinger/sdk';

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

# **listNodeJsEnvironmentVariablesV1**
> Array<HostingV1NodeJsEnvVarResource> listNodeJsEnvironmentVariablesV1()

Lists the Node.js environment variables currently set for the website. Values are always masked as `********` and cannot be read back through this API. Use this endpoint to see which keys are configured or to verify a change, not to read values.  To change variables, use the `Replace Node.js environment variables` endpoint. It replaces the whole set, so never copy the masked values from this response into that request; send the full desired set with real values taken from the project `.env` file or the user prompt instead.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.listNodeJsEnvironmentVariablesV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**Array<HostingV1NodeJsEnvVarResource>**

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

# **listNodeJsVulnerabilitiesV1**
> Array<HostingV1NodeJsVulnerabilityResource> listNodeJsVulnerabilitiesV1()

Lists known npm package vulnerabilities detected on a Node.js website, enriched with advisory metadata (severity, CVSS score, CVE, advisory URL). Results are sorted from the most severe to the least severe, then by publish date (newest first). Use the `severities` query parameter to filter.  Vulnerabilities with `is_patchable` set to `true` can be auto-fixed via the `Patch Node.js Vulnerabilities` endpoint, which opens a GitHub pull request with updated package versions. Auto-fix is only available for websites deployed from a connected GitHub repository. Vulnerabilities with `is_patching_in_progress` set to `true` are already included in an open patch pull request; while any patch pull request is open, new patch requests for this website are rejected until it is merged or closed.  Data comes from periodic dependency scans, so it may lag behind the latest deployment. An empty list means the most recent scan found no vulnerabilities; it does not guarantee the current deployment is vulnerability-free. Available on Business and Cloud Hosting plans.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let severities: Array<'low' | 'moderate' | 'high' | 'critical' | 'unknown'>; //Severities to filter by (optional) (default to undefined)

const { status, data } = await apiInstance.listNodeJsVulnerabilitiesV1(
    username,
    domain,
    severities
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **severities** | **Array<&#39;low&#39; &#124; &#39;moderate&#39; &#124; &#39;high&#39; &#124; &#39;critical&#39; &#124; &#39;unknown&#39;>** | Severities to filter by | (optional) defaults to undefined|


### Return type

**Array<HostingV1NodeJsVulnerabilityResource>**

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

# **patchNodeJsVulnerabilitiesV1**
> HostingV1NodeJsPatchResultResource patchNodeJsVulnerabilitiesV1(hostingV1NodeJsPatchVulnerabilitiesRequest)

Patches the selected Node.js vulnerabilities by updating the affected package versions in `package.json` and opening a GitHub pull request in the connected repository. The customer reviews and merges the pull request; merging triggers the automatic deployment.  Auto-fix is only available for websites deployed from a connected GitHub repository. Websites deployed from an archive have no auto-fix path and return a 404. The Hostinger GitHub App needs write access to the repository; without it the request fails with a 403 explaining the missing permission.  Only vulnerabilities with `is_patchable` set to `true` can be patched. Non-patchable IDs in the selection are skipped; the pull request covers the patchable subset, listed in `patched_vulnerability_ids`. Selections without any patchable vulnerability are rejected with a 422. Only one patch pull request can be open at a time per website; close or merge it before patching again. Available on Business and Cloud Hosting plans.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration,
    HostingV1NodeJsPatchVulnerabilitiesRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1NodeJsPatchVulnerabilitiesRequest: HostingV1NodeJsPatchVulnerabilitiesRequest; //

const { status, data } = await apiInstance.patchNodeJsVulnerabilitiesV1(
    username,
    domain,
    hostingV1NodeJsPatchVulnerabilitiesRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1NodeJsPatchVulnerabilitiesRequest** | **HostingV1NodeJsPatchVulnerabilitiesRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1NodeJsPatchResultResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replaceNodeJsEnvironmentVariablesV1**
> CommonSuccessEmptyResource replaceNodeJsEnvironmentVariablesV1(hostingV1NodeJsSetBuildEnvVarsRequest)

Replaces the website\'s Node.js environment variables with the ones provided. This is a full replace: any variable not in the request is deleted, and sending an empty `env_vars` array deletes every variable. Saving writes the values and restarts the running Node.js process.  A restart is enough for apps that read environment variables at process start, such as Express or NestJS. It is not enough for frameworks that bake variables into the build. Next.js standalone is one of those: build-time values (including `NEXT_PUBLIC_*`) need a fresh build. After this call, use the `Start Node.js build` endpoint so those apps pick up the new values.  The `List Node.js environment variables` endpoint returns masked values (`********`), so never copy values from it into this request. Always send the full desired set with real values taken from the project `.env` file or the user prompt.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration,
    HostingV1NodeJsSetBuildEnvVarsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1NodeJsSetBuildEnvVarsRequest: HostingV1NodeJsSetBuildEnvVarsRequest; //

const { status, data } = await apiInstance.replaceNodeJsEnvironmentVariablesV1(
    username,
    domain,
    hostingV1NodeJsSetBuildEnvVarsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1NodeJsSetBuildEnvVarsRequest** | **HostingV1NodeJsSetBuildEnvVarsRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **restartNodeJsApplicationV1**
> CommonSuccessEmptyResource restartNodeJsApplicationV1()

Restarts the Node.js server process for the website. Does not rebuild or redeploy the application. Use it to apply environment or configuration changes, or to recover a hung application.  Only applicable to server-side applications (Express, Next.js, NestJS, etc.). Static front-end apps (React, Vue, Vite) have no persistent server process, so restarting them has no effect. Returns success even when the website has no server process to restart.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.restartNodeJsApplicationV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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

# **startNodeJsBuildV1**
> HostingV1NodeJsBuildResource startNodeJsBuildV1(hostingV1NodeJsStartBuildRequest)

Start a Node.js build process using files already present on the website\'s file storage.  WARNING: on success this overwrites the website\'s existing contents and cannot be undone — verify this is intended before calling this endpoint.  The `source_type` must be `archive` and `source_options.archive_path` must point to an existing archive file on the server (relative to the website document root). Use the `Generate Upload URL` endpoint to obtain credentials and upload the archive first.  To auto-detect build settings from an archive before starting, first call the `Get Node.js Build Settings from Archive` endpoint.  The returned build `uuid` can be used to poll progress and retrieve logs via the `Get Node.js Build Logs` endpoint.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration,
    HostingV1NodeJsStartBuildRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1NodeJsStartBuildRequest: HostingV1NodeJsStartBuildRequest; //

const { status, data } = await apiInstance.startNodeJsBuildV1(
    username,
    domain,
    hostingV1NodeJsStartBuildRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1NodeJsStartBuildRequest** | **HostingV1NodeJsStartBuildRequest**|  | |
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

# **updateNodeJsBuildSettingsV1**
> HostingV1NodeJsStoredBuildSettingsResource updateNodeJsBuildSettingsV1(hostingV1NodeJsUpdateBuildSettingsRequest)

Replaces the build settings stored for the website. Send the full set: `node_version` is required and every nullable field you omit is stored as null. Creates the settings when none exist yet.  This does not start a build. Stored settings drive Git auto-deployment builds; a build started through the API uses the values sent in that request, so to rebuild with corrected settings call `Start Node.js build` with the same values. Typical fixes: a wrong `app_type` after auto-detection, or a missing `entry_file` for express, fastify, nest, nuxt and hono apps.

### Example

```typescript
import {
    HostingNodeJSApi,
    Configuration,
    HostingV1NodeJsUpdateBuildSettingsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingNodeJSApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1NodeJsUpdateBuildSettingsRequest: HostingV1NodeJsUpdateBuildSettingsRequest; //

const { status, data } = await apiInstance.updateNodeJsBuildSettingsV1(
    username,
    domain,
    hostingV1NodeJsUpdateBuildSettingsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1NodeJsUpdateBuildSettingsRequest** | **HostingV1NodeJsUpdateBuildSettingsRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1NodeJsStoredBuildSettingsResource**

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

