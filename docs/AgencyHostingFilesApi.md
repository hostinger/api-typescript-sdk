# AgencyHostingFilesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**generateUploadURLV1**](#generateuploadurlv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/files/upload-urls | Generate upload URL|
|[**importWebsiteFromArchiveV1**](#importwebsitefromarchivev1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/files/import-archive | Import website from archive|

# **generateUploadURLV1**
> AgencyHostingV1FilesUploadUrlResource generateUploadURLV1()

Generate a file browser upload URL with authentication credentials for uploading files to an Agency Plan website\'s file storage.  Returns `url`, `auth_key` and `rest_auth_key`. Use these to upload a file to the website\'s file storage via the TUS resumable upload protocol (TUS 1.0.0). Send `X-Auth: {auth_key}` and `X-Auth-Rest: {rest_auth_key}` headers on every request below.  1. Create the upload: `POST` to `{url}/{relative_file_path}?override=true` with headers    `upload-length: {file size in bytes}` and `upload-offset: 0`. Expect `201 Created`. 2. Upload the file: send the file bytes to the same location (any TUS 1.0.0 client, or    `PATCH` requests with an `upload-offset` header tracking progress) until complete.  `relative_file_path` is the destination path inside the website\'s file storage, e.g. `app.zip`.  Instead of a TUS client, plain `curl` also works: ``` FILE=app.zip SIZE=$(stat -f%z \"$FILE\")   # stat -c%s on Linux  curl -i -X POST \"{url}/${FILE}?override=true\" \\   -H \"X-Auth: {auth_key}\" \\   -H \"X-Auth-Rest: {rest_auth_key}\" \\   -H \"Tus-Resumable: 1.0.0\" \\   -H \"Upload-Length: ${SIZE}\" \\   -H \"Upload-Offset: 0\" # -> 201 Created  curl -i -X PATCH \"{url}/${FILE}?override=true\" \\   -H \"X-Auth: {auth_key}\" \\   -H \"X-Auth-Rest: {rest_auth_key}\" \\   -H \"Tus-Resumable: 1.0.0\" \\   -H \"Content-Type: application/offset+octet-stream\" \\   -H \"Upload-Offset: 0\" \\   --data-binary \"@${FILE}\" # -> 204 No Content, Upload-Offset response header equals SIZE when done ```

### Example

```typescript
import {
    AgencyHostingFilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingFilesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.generateUploadURLV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**AgencyHostingV1FilesUploadUrlResource**

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

# **importWebsiteFromArchiveV1**
> CommonSuccessEmptyResource importWebsiteFromArchiveV1(agencyHostingV1FilesImportArchiveRequest)

Imports an Agency Plan website from an already-uploaded archive.  Upload the archive to the website\'s root directory via file browser first, then provide its filename in this request. Website contents are overwritten by the archive contents. Supported archive types: .zip, .tar, .tar.gz, .tgz.

### Example

```typescript
import {
    AgencyHostingFilesApi,
    Configuration,
    AgencyHostingV1FilesImportArchiveRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingFilesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1FilesImportArchiveRequest: AgencyHostingV1FilesImportArchiveRequest; //

const { status, data } = await apiInstance.importWebsiteFromArchiveV1(
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

