# AgencyHostingFilesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**importAgencyPlanWebsiteFromArchiveV1**](#importagencyplanwebsitefromarchivev1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/files/import-archive | Import Agency Plan website from archive|

# **importAgencyPlanWebsiteFromArchiveV1**
> CommonSuccessEmptyResource importAgencyPlanWebsiteFromArchiveV1(agencyHostingV1FilesImportArchiveRequest)

Imports an Agency Plan website from an already-uploaded archive.  Upload the archive to the website\'s root directory via file browser first, then provide its filename in this request. Website contents are overwritten by the archive contents. Supported archive types: .zip, .tar, .tar.gz, .tgz.

### Example

```typescript
import {
    AgencyHostingFilesApi,
    Configuration,
    AgencyHostingV1FilesImportArchiveRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingFilesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1FilesImportArchiveRequest: AgencyHostingV1FilesImportArchiveRequest; //

const { status, data } = await apiInstance.importAgencyPlanWebsiteFromArchiveV1(
    websiteUid,
    agencyHostingV1FilesImportArchiveRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1FilesImportArchiveRequest** | **AgencyHostingV1FilesImportArchiveRequest**|  | |
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

