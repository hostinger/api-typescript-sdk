# HostingGitApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listGitInstallationRepositoriesV1**](#listgitinstallationrepositoriesv1) | **GET** /api/hosting/v1/git/installations/{uuid}/repositories | List Git installation repositories|
|[**listGitInstallationsV1**](#listgitinstallationsv1) | **GET** /api/hosting/v1/git/installations | List Git installations|

# **listGitInstallationRepositoriesV1**
> Array<HostingV1GitGitRepositoryResource> listGitInstallationRepositoriesV1()

Lists the repositories the Git installation can access, read live from the provider. Works for github and gitlab installations. Use an active installation: a suspended or pending one is still queried and the call fails with whatever the provider answers. The list is cut at the first 500 repositories in the order the provider returns them; when the account has more, name the repository directly instead of searching this list.  `owner`, `name` and `default_branch` identify a repository and a branch to deploy. Returns 404 when the installation does not belong to the customer. Limited to 10 calls per minute per API client (429 above that).

### Example

```typescript
import {
    HostingGitApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingGitApi(configuration);

let uuid: string; //Git installation UUID from the List Git installations endpoint (default to undefined)

const { status, data } = await apiInstance.listGitInstallationRepositoriesV1(
    uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | [**string**] | Git installation UUID from the List Git installations endpoint | defaults to undefined|


### Return type

**Array<HostingV1GitGitRepositoryResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**404** | Error response |  -  |
|**429** | Error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listGitInstallationsV1**
> Array<HostingV1GitGitInstallationResource> listGitInstallationsV1()

Lists the Git provider accounts the customer has connected. Only installations with status `active` are returned unless the `status` filter says otherwise.  An empty list means the customer has no active installation. Check `status=suspended` and `status=pending` as well. If there is none at all, GitHub has to be connected once in hPanel (Websites, Manage, Advanced, Git, Connect GitHub; or Add Website, Node.js Web App, Import Git Repository, Continue with GitHub); this endpoint then lists the new installation.  Use `uuid` as the path parameter of `List Git installation repositories`.

### Example

```typescript
import {
    HostingGitApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingGitApi(configuration);

let provider: 'github' | 'gitlab' | 'bitbucket'; //Filter by Git provider (optional) (default to undefined)
let status: 'pending' | 'active' | 'suspended'; //Filter by installation status (optional) (default to 'active')

const { status, data } = await apiInstance.listGitInstallationsV1(
    provider,
    status
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **provider** | [**&#39;github&#39; | &#39;gitlab&#39; | &#39;bitbucket&#39;**]**Array<&#39;github&#39; &#124; &#39;gitlab&#39; &#124; &#39;bitbucket&#39;>** | Filter by Git provider | (optional) defaults to undefined|
| **status** | [**&#39;pending&#39; | &#39;active&#39; | &#39;suspended&#39;**]**Array<&#39;pending&#39; &#124; &#39;active&#39; &#124; &#39;suspended&#39;>** | Filter by installation status | (optional) defaults to 'active'|


### Return type

**Array<HostingV1GitGitInstallationResource>**

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

