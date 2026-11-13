# GPUInstancesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createInstanceV1**](#createinstancev1) | **POST** /api/gpu/v1/instances | Create instance|
|[**deleteInstanceV1**](#deleteinstancev1) | **DELETE** /api/gpu/v1/instances/{instanceId} | Delete instance|
|[**getInstanceDetailsV1**](#getinstancedetailsv1) | **GET** /api/gpu/v1/instances/{instanceId} | Get instance details|
|[**getInstanceMetricsV1**](#getinstancemetricsv1) | **GET** /api/gpu/v1/instances/{instanceId}/metrics | Get instance metrics|
|[**getInstancesV1**](#getinstancesv1) | **GET** /api/gpu/v1/instances | Get instances|

# **createInstanceV1**
> CommonSuccessEmptyResource createInstanceV1(gPUV1InstanceStoreRequest)

Create a new GPU instance.  Pick `pool_instance_id` from the pool instance types list and `os_template_id` from the OS templates available for that instance type. Your account must have enough credits to run the instance for its first hour.  The instance is created asynchronously: a successful request returns immediately, and the instance appears in the instance list while its `status` moves from `created` through `creating` to `running`.  Use this endpoint to provision GPU compute.

### Example

```typescript
import {
    GPUInstancesApi,
    Configuration,
    GPUV1InstanceStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUInstancesApi(configuration);

let gPUV1InstanceStoreRequest: GPUV1InstanceStoreRequest; //

const { status, data } = await apiInstance.createInstanceV1(
    gPUV1InstanceStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **gPUV1InstanceStoreRequest** | **GPUV1InstanceStoreRequest**|  | |


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

# **deleteInstanceV1**
> CommonSuccessEmptyResource deleteInstanceV1()

Delete a specified GPU instance.  The instance is destroyed asynchronously: a successful request returns immediately and the instance `status` moves to `destroying`. Deleting fails while the instance is in `created`, `destroying`, `destroyed` or `abuse` status, or while another action is in progress on it.  Use this endpoint to stop billing for a GPU instance you no longer need.

### Example

```typescript
import {
    GPUInstancesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUInstancesApi(configuration);

let instanceId: number; //GPU instance ID (default to undefined)

const { status, data } = await apiInstance.deleteInstanceV1(
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **instanceId** | [**number**] | GPU instance ID | defaults to undefined|


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

# **getInstanceDetailsV1**
> GPUV1InstanceInstanceResource getInstanceDetailsV1()

Retrieve detailed information about a specified GPU instance, including its SSH keys.  Use this endpoint to follow the instance `status` after creating or deleting it.

### Example

```typescript
import {
    GPUInstancesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUInstancesApi(configuration);

let instanceId: number; //GPU instance ID (default to undefined)

const { status, data } = await apiInstance.getInstanceDetailsV1(
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **instanceId** | [**number**] | GPU instance ID | defaults to undefined|


### Return type

**GPUV1InstanceInstanceResource**

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

# **getInstanceMetricsV1**
> Array<GPUV1MetricsMetricsResource> getInstanceMetricsV1()

Retrieve utilisation metrics of a specified GPU instance for the last hour.  Each data point contains CPU, memory and GPU utilisation, used GPU memory and GPU throughput. The list is empty until the instance is provisioned.  Use this endpoint to monitor GPU instance load.

### Example

```typescript
import {
    GPUInstancesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUInstancesApi(configuration);

let instanceId: number; //GPU instance ID (default to undefined)

const { status, data } = await apiInstance.getInstanceMetricsV1(
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **instanceId** | [**number**] | GPU instance ID | defaults to undefined|


### Return type

**Array<GPUV1MetricsMetricsResource>**

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

# **getInstancesV1**
> Array<GPUV1InstanceInstanceListResource> getInstancesV1()

Retrieve all GPU instances of your account.  Use this endpoint to view your GPU instances with their status, pool, instance type and OS template.

### Example

```typescript
import {
    GPUInstancesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUInstancesApi(configuration);

const { status, data } = await apiInstance.getInstancesV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<GPUV1InstanceInstanceListResource>**

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

