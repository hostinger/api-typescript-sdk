# WordPressMaintenanceApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**showMaintenanceStatusV1**](#showmaintenancestatusv1) | **GET** /api/hosting/v1/accounts/{username}/wordpress/{software}/maintenance/status | Show maintenance status|
|[**toggleMaintenanceModeV1**](#togglemaintenancemodev1) | **PATCH** /api/hosting/v1/accounts/{username}/wordpress/{software}/maintenance/toggle | Toggle maintenance mode|

# **showMaintenanceStatusV1**
> WordPressV1MaintenanceMaintenanceStatusResource showMaintenanceStatusV1()

Show the maintenance mode status for the specified WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressMaintenanceApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressMaintenanceApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.showMaintenanceStatusV1(
    username,
    software
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|


### Return type

**WordPressV1MaintenanceMaintenanceStatusResource**

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

# **toggleMaintenanceModeV1**
> CommonSuccessEmptyResource toggleMaintenanceModeV1(wordPressV1MaintenanceToggleMaintenanceRequest)

Enable or disable maintenance mode for the specified WordPress installation, based on the `enabled` flag.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressMaintenanceApi,
    Configuration,
    WordPressV1MaintenanceToggleMaintenanceRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressMaintenanceApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)
let wordPressV1MaintenanceToggleMaintenanceRequest: WordPressV1MaintenanceToggleMaintenanceRequest; //

const { status, data } = await apiInstance.toggleMaintenanceModeV1(
    username,
    software,
    wordPressV1MaintenanceToggleMaintenanceRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **wordPressV1MaintenanceToggleMaintenanceRequest** | **WordPressV1MaintenanceToggleMaintenanceRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|


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

