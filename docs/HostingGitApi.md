# HostingGitApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteGitAutoDeploymentSettingsV1**](#deletegitautodeploymentsettingsv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/git/auto-deployments/settings | Delete Git auto-deployment settings|
|[**getGitAutoDeploymentSettingsV1**](#getgitautodeploymentsettingsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/git/auto-deployments/settings | Get Git auto-deployment settings|
|[**listGitInstallationRepositoriesV1**](#listgitinstallationrepositoriesv1) | **GET** /api/hosting/v1/git/installations/{uuid}/repositories | List Git installation repositories|
|[**listGitInstallationsV1**](#listgitinstallationsv1) | **GET** /api/hosting/v1/git/installations | List Git installations|
|[**updateGitAutoDeploymentSettingsV1**](#updategitautodeploymentsettingsv1) | **PUT** /api/hosting/v1/accounts/{username}/websites/{domain}/git/auto-deployments/settings | Update Git auto-deployment settings|

# **deleteGitAutoDeploymentSettingsV1**
> CommonSuccessEmptyResource deleteGitAutoDeploymentSettingsV1()

Removes the Git auto-deployment settings of the website. Files already deployed stay on the website; pushes stop deploying until settings are saved again. Succeeds also when nothing is configured.

### Example

```typescript
import {
    HostingGitApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingGitApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.deleteGitAutoDeploymentSettingsV1(
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

# **getGitAutoDeploymentSettingsV1**
> HostingV1GitGitAutoDeploymentSettingsResource getGitAutoDeploymentSettingsV1()

Returns the Git auto-deployment settings of the website: which repository and branch deploy into which directory, and whether pushes trigger a deployment. `is_enabled` false keeps the repository link but ignores pushes.  When the website has no auto-deployment configured every field is null. Save settings with `Update Git auto-deployment settings`.

### Example

```typescript
import {
    HostingGitApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingGitApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getGitAutoDeploymentSettingsV1(
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

**HostingV1GitGitAutoDeploymentSettingsResource**

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

# **listGitInstallationRepositoriesV1**
> Array<HostingV1GitGitRepositoryResource> listGitInstallationRepositoriesV1()

Lists the repositories the Git installation can access, read live from the provider. Works for github and gitlab installations. Use an active installation: a suspended or pending one is still queried and the call fails with whatever the provider answers. The list is cut at the first 500 repositories in the order the provider returns them; when the account has more, name the repository directly instead of searching this list.  `owner`, `name` and a branch (`default_branch` or another one) go into `source_options` of `Start Node.js build` or into `Update Git auto-deployment settings`. Returns 404 when the installation does not belong to the customer. Limited to 10 calls per minute per API client (429 above that).

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

Lists the Git provider accounts the customer has connected. Only installations with status `active` are returned unless the `status` filter says otherwise.  An empty list means the customer has no active installation. Check `status=suspended` and `status=pending` as well. If there is none at all, a Git provider (GitHub or GitLab) has to be connected once in hPanel (Websites, Manage, Advanced, Git; or Add Website, Node.js Web App, Import Git Repository); this endpoint then lists the new installation.  Use `uuid` as the path parameter of `List Git installation repositories`, and as `installation_uuid` in `Start Node.js build` with `source_type` `git` and in `Update Git auto-deployment settings`.

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

# **updateGitAutoDeploymentSettingsV1**
> CommonSuccessEmptyResource updateGitAutoDeploymentSettingsV1(hostingV1GitUpdateGitAutoDeploymentSettingsRequest)

Creates or replaces the Git auto-deployment settings of the website: repository, branch, the directory under the document root to deploy into, and `is_enabled`. Send the full set; `is_enabled` defaults to true and `directory` to the document root. `installation_uuid` must be an installation from `List Git installations` that belongs to the same customer as the website.  For PHP and static websites, saving with `is_enabled` true deploys the branch right away and every later push to that branch deploys again. For Node.js and Website Builder websites saving does not clone anything. On a Node.js website start the first deploy with `Start Node.js build` using `source_type` `git`; pushes then trigger new builds with the build settings stored for the website.

### Example

```typescript
import {
    HostingGitApi,
    Configuration,
    HostingV1GitUpdateGitAutoDeploymentSettingsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingGitApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1GitUpdateGitAutoDeploymentSettingsRequest: HostingV1GitUpdateGitAutoDeploymentSettingsRequest; //

const { status, data } = await apiInstance.updateGitAutoDeploymentSettingsV1(
    username,
    domain,
    hostingV1GitUpdateGitAutoDeploymentSettingsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1GitUpdateGitAutoDeploymentSettingsRequest** | **HostingV1GitUpdateGitAutoDeploymentSettingsRequest**|  | |
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

