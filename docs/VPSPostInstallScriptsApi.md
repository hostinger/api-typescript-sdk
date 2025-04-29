# VPSPostInstallScriptsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createPostInstallScriptV1**](#createpostinstallscriptv1) | **POST** /api/vps/v1/post-install-scripts | Create post-install script|
|[**deleteAPostInstallScriptV1**](#deleteapostinstallscriptv1) | **DELETE** /api/vps/v1/post-install-scripts/{postInstallScriptId} | Delete a post-install script|
|[**getPostInstallScriptListV1**](#getpostinstallscriptlistv1) | **GET** /api/vps/v1/post-install-scripts | Get post-install script list|
|[**getPostInstallScriptV1**](#getpostinstallscriptv1) | **GET** /api/vps/v1/post-install-scripts/{postInstallScriptId} | Get post-install script|
|[**updatePostInstallScriptV1**](#updatepostinstallscriptv1) | **PUT** /api/vps/v1/post-install-scripts/{postInstallScriptId} | Update post-install script|

# **createPostInstallScriptV1**
> VPSV1PostInstallScriptPostInstallScriptResource createPostInstallScriptV1(vPSV1PostInstallScriptStoreRequest)

This endpoint allows you to add a new post-install script to your account,  which can then be used run after the installation of a virtual machine instance.  The script contents will be saved to the file `/post_install` with executable attribute set and will be executed once virtual machine is installed. The output of the script will be redirected to `/post_install.log`. Maximum script size is 48KB. 

### Example

```typescript
import {
    VPSPostInstallScriptsApi,
    Configuration,
    VPSV1PostInstallScriptStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPostInstallScriptsApi(configuration);

let vPSV1PostInstallScriptStoreRequest: VPSV1PostInstallScriptStoreRequest; //

const { status, data } = await apiInstance.createPostInstallScriptV1(
    vPSV1PostInstallScriptStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1PostInstallScriptStoreRequest** | **VPSV1PostInstallScriptStoreRequest**|  | |


### Return type

**VPSV1PostInstallScriptPostInstallScriptResource**

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAPostInstallScriptV1**
> CommonSuccessEmptyResource deleteAPostInstallScriptV1()

This endpoint deletes a post-install script from your account. 

### Example

```typescript
import {
    VPSPostInstallScriptsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPostInstallScriptsApi(configuration);

let postInstallScriptId: number; //Post-install script ID (default to undefined)

const { status, data } = await apiInstance.deleteAPostInstallScriptV1(
    postInstallScriptId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **postInstallScriptId** | [**number**] | Post-install script ID | defaults to undefined|


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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPostInstallScriptListV1**
> VPSGetPostInstallScriptListV1200Response getPostInstallScriptListV1()

This endpoint retrieves a list of post-install scripts associated with your account.

### Example

```typescript
import {
    VPSPostInstallScriptsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPostInstallScriptsApi(configuration);

let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getPostInstallScriptListV1(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**VPSGetPostInstallScriptListV1200Response**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPostInstallScriptV1**
> VPSV1PostInstallScriptPostInstallScriptResource getPostInstallScriptV1()

This endpoint retrieves post-install script by its ID.

### Example

```typescript
import {
    VPSPostInstallScriptsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPostInstallScriptsApi(configuration);

let postInstallScriptId: number; //Post-install script ID (default to undefined)

const { status, data } = await apiInstance.getPostInstallScriptV1(
    postInstallScriptId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **postInstallScriptId** | [**number**] | Post-install script ID | defaults to undefined|


### Return type

**VPSV1PostInstallScriptPostInstallScriptResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updatePostInstallScriptV1**
> VPSV1PostInstallScriptPostInstallScriptResource updatePostInstallScriptV1(vPSV1PostInstallScriptStoreRequest)

This endpoint updates a specific post-install script.

### Example

```typescript
import {
    VPSPostInstallScriptsApi,
    Configuration,
    VPSV1PostInstallScriptStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPostInstallScriptsApi(configuration);

let postInstallScriptId: number; //Post-install script ID (default to undefined)
let vPSV1PostInstallScriptStoreRequest: VPSV1PostInstallScriptStoreRequest; //

const { status, data } = await apiInstance.updatePostInstallScriptV1(
    postInstallScriptId,
    vPSV1PostInstallScriptStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1PostInstallScriptStoreRequest** | **VPSV1PostInstallScriptStoreRequest**|  | |
| **postInstallScriptId** | [**number**] | Post-install script ID | defaults to undefined|


### Return type

**VPSV1PostInstallScriptPostInstallScriptResource**

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

