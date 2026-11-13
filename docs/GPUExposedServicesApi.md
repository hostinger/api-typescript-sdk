# GPUExposedServicesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createExposedServiceV1**](#createexposedservicev1) | **POST** /api/gpu/v1/instances/{instanceId}/exposed-services | Create exposed service|
|[**deleteExposedServiceV1**](#deleteexposedservicev1) | **DELETE** /api/gpu/v1/instances/{instanceId}/exposed-services/{exposedServiceId} | Delete exposed service|
|[**getExposedServicesV1**](#getexposedservicesv1) | **GET** /api/gpu/v1/instances/{instanceId}/exposed-services | Get exposed services|

# **createExposedServiceV1**
> CommonSuccessEmptyResource createExposedServiceV1(gPUV1ExposedServiceStoreRequest)

Expose a service running on a specified GPU instance to the internet.  The service is exposed asynchronously: a successful request returns immediately, and the service appears in the exposed services list once it gets its public hostname and external port. Fails when the instance already has the maximum of 4 exposed services.  Use this endpoint to make an application on your GPU instance publicly reachable.

### Example

```typescript
import {
    GPUExposedServicesApi,
    Configuration,
    GPUV1ExposedServiceStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUExposedServicesApi(configuration);

let instanceId: number; //GPU instance ID (default to undefined)
let gPUV1ExposedServiceStoreRequest: GPUV1ExposedServiceStoreRequest; //

const { status, data } = await apiInstance.createExposedServiceV1(
    instanceId,
    gPUV1ExposedServiceStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **gPUV1ExposedServiceStoreRequest** | **GPUV1ExposedServiceStoreRequest**|  | |
| **instanceId** | [**number**] | GPU instance ID | defaults to undefined|


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
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteExposedServiceV1**
> CommonSuccessEmptyResource deleteExposedServiceV1()

Delete a specified exposed service of a GPU instance.  The service is removed asynchronously: a successful request returns immediately and the service stops being reachable from the internet shortly after.  Use this endpoint to close public access to a service on your GPU instance.

### Example

```typescript
import {
    GPUExposedServicesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUExposedServicesApi(configuration);

let instanceId: number; //GPU instance ID (default to undefined)
let exposedServiceId: number; //Exposed service ID (default to undefined)

const { status, data } = await apiInstance.deleteExposedServiceV1(
    instanceId,
    exposedServiceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **instanceId** | [**number**] | GPU instance ID | defaults to undefined|
| **exposedServiceId** | [**number**] | Exposed service ID | defaults to undefined|


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
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getExposedServicesV1**
> Array<GPUV1ExposedServiceExposedServiceResource> getExposedServicesV1()

Retrieve the services exposed on a specified GPU instance.  A newly created service is listed once it gets its public hostname and external port.  Use this endpoint to find the public address of services running on your GPU instance.

### Example

```typescript
import {
    GPUExposedServicesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUExposedServicesApi(configuration);

let instanceId: number; //GPU instance ID (default to undefined)

const { status, data } = await apiInstance.getExposedServicesV1(
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **instanceId** | [**number**] | GPU instance ID | defaults to undefined|


### Return type

**Array<GPUV1ExposedServiceExposedServiceResource>**

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

