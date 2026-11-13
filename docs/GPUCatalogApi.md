# GPUCatalogApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getPoolGroupsV1**](#getpoolgroupsv1) | **GET** /api/gpu/v1/pools/groups | Get pool groups|
|[**getPoolInstanceTypesV1**](#getpoolinstancetypesv1) | **GET** /api/gpu/v1/pools/{poolId}/instances | Get pool instance types|
|[**getPoolListV1**](#getpoollistv1) | **GET** /api/gpu/v1/pools | Get pool list|
|[**getPoolOSTemplatesV1**](#getpoolostemplatesv1) | **GET** /api/gpu/v1/pools/{poolId}/instances/{poolInstanceId}/os-templates | Get pool OS templates|

# **getPoolGroupsV1**
> Array<GPUV1PoolPoolGroupResource> getPoolGroupsV1()

Retrieve GPU pool groups, ordered by name.  Each group bundles the pools of one GPU model and lists its currently available pools, whether any of them is available and the lowest hourly price, in credits, among its instance types. The price is returned even when the group is out of stock.  Use this endpoint to show which GPU models can be ordered and from what price.

### Example

```typescript
import {
    GPUCatalogApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUCatalogApi(configuration);

const { status, data } = await apiInstance.getPoolGroupsV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<GPUV1PoolPoolGroupResource>**

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

# **getPoolInstanceTypesV1**
> Array<GPUV1PoolPoolInstanceResource> getPoolInstanceTypesV1()

Retrieve the instance types offered by a specified GPU pool, ordered by CPU core count.  Each instance type describes its CPU, memory and storage, and its hourly price. Only instance types that can currently be ordered are returned.  Use this endpoint to choose the `pool_instance_id` for a new GPU instance.

### Example

```typescript
import {
    GPUCatalogApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUCatalogApi(configuration);

let poolId: number; //GPU pool ID (default to undefined)

const { status, data } = await apiInstance.getPoolInstanceTypesV1(
    poolId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **poolId** | [**number**] | GPU pool ID | defaults to undefined|


### Return type

**Array<GPUV1PoolPoolInstanceResource>**

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
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPoolListV1**
> Array<GPUV1PoolPoolResource> getPoolListV1()

Retrieve all available GPU pools, ordered by name.  A pool serves GPU accelerators of one model from a single region.  Use this endpoint to choose a pool before listing its instance types.

### Example

```typescript
import {
    GPUCatalogApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUCatalogApi(configuration);

const { status, data } = await apiInstance.getPoolListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<GPUV1PoolPoolResource>**

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

# **getPoolOSTemplatesV1**
> Array<GPUV1OsTemplateOsTemplateResource> getPoolOSTemplatesV1()

Retrieve the OS templates that can be installed on a specified GPU pool instance type.  Use this endpoint to choose the `os_template_id` for a new GPU instance.

### Example

```typescript
import {
    GPUCatalogApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUCatalogApi(configuration);

let poolId: number; //GPU pool ID (default to undefined)
let poolInstanceId: number; //GPU pool instance type ID (default to undefined)

const { status, data } = await apiInstance.getPoolOSTemplatesV1(
    poolId,
    poolInstanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **poolId** | [**number**] | GPU pool ID | defaults to undefined|
| **poolInstanceId** | [**number**] | GPU pool instance type ID | defaults to undefined|


### Return type

**Array<GPUV1OsTemplateOsTemplateResource>**

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
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

