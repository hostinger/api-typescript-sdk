# HostingFilesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getWebsiteFileContentV1**](#getwebsitefilecontentv1) | **GET** /api/hosting/v1/accounts/{username}/domains/{domain}/files/content | Get website file content|
|[**listWebsiteFilesAndDirectoriesV1**](#listwebsitefilesanddirectoriesv1) | **GET** /api/hosting/v1/accounts/{username}/domains/{domain}/files | List website files and directories|

# **getWebsiteFileContentV1**
> HostingV1FilesFileContentResource getWebsiteFileContentV1()

Get a single file\'s content, relative to a website\'s document root.  Read-only; refuses symlinks, oversized files, non-text file types, and files identified as containing secrets (e.g. credential files) — none of these are returned by this endpoint.

### Example

```typescript
import {
    HostingFilesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingFilesApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let path: string; //File path, relative to the document root. (default to undefined)
let fromLine: number; //Line offset to start reading from. (optional) (default to 0)
let maxLines: number; //Max number of lines to return. (optional) (default to 5000)

const { status, data } = await apiInstance.getWebsiteFileContentV1(
    username,
    domain,
    path,
    fromLine,
    maxLines
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **path** | [**string**] | File path, relative to the document root. | defaults to undefined|
| **fromLine** | [**number**] | Line offset to start reading from. | (optional) defaults to 0|
| **maxLines** | [**number**] | Max number of lines to return. | (optional) defaults to 5000|


### Return type

**HostingV1FilesFileContentResource**

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

# **listWebsiteFilesAndDirectoriesV1**
> HostingV1FilesFilesResource listWebsiteFilesAndDirectoriesV1()

List files and directories under a website\'s document root.  Use `directory` to browse a subdirectory relative to the document root. Symlinked entries are listed but never traversed into or resolved.

### Example

```typescript
import {
    HostingFilesApi,
    Configuration,
    HostingListWebsiteFilesAndDirectoriesV1FileTypesParameter
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingFilesApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let directory: string; //Directory path to check (optional) (default to '')
let maxDepth: number; //How many directory levels deep to recurse. (optional) (default to 5)
let maxItems: number; //Max number of entries to return in this page. (optional) (default to 1000)
let offset: number; //Number of entries to skip. Page with offset + item count until reaching total_items. (optional) (default to 0)
let fileTypes: HostingListWebsiteFilesAndDirectoriesV1FileTypesParameter; //Filter by entry type, e.g. file,directory. Array or comma-separated. Omit for all types. (optional) (default to undefined)

const { status, data } = await apiInstance.listWebsiteFilesAndDirectoriesV1(
    username,
    domain,
    directory,
    maxDepth,
    maxItems,
    offset,
    fileTypes
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **directory** | [**string**] | Directory path to check | (optional) defaults to ''|
| **maxDepth** | [**number**] | How many directory levels deep to recurse. | (optional) defaults to 5|
| **maxItems** | [**number**] | Max number of entries to return in this page. | (optional) defaults to 1000|
| **offset** | [**number**] | Number of entries to skip. Page with offset + item count until reaching total_items. | (optional) defaults to 0|
| **fileTypes** | **HostingListWebsiteFilesAndDirectoriesV1FileTypesParameter** | Filter by entry type, e.g. file,directory. Array or comma-separated. Omit for all types. | (optional) defaults to undefined|


### Return type

**HostingV1FilesFilesResource**

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

