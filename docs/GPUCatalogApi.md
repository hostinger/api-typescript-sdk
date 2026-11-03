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

Retrieve GPU pool groups, ordered by name.  Each group bundles the pools of one GPU model and lists its currently available pools, whether any of them is available and the lowest hourly price among its instance types. The price is returned even when the group is out of stock.  Use this endpoint to show which GPU models can be ordered and from what price.

### Example

```typescript
import {
    GPUCatalogApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new GPUCatalogApi(configuration);

let currency: 'USD' | 'ARS' | 'AMD' | 'AUD' | 'AZN' | 'BDT' | 'BRL' | 'BTC' | 'BYN' | 'CAD' | 'CHF' | 'CLP' | 'CNY' | 'COP' | 'CZK' | 'DKK' | 'EGP' | 'EUR' | 'GBP' | 'GEL' | 'HKD' | 'HRK' | 'HUF' | 'IDR' | 'ILS' | 'INR' | 'JPY' | 'KGS' | 'KRW' | 'KZT' | 'MAD' | 'MXN' | 'MYR' | 'NGN' | 'NOK' | 'NZD' | 'PEN' | 'PHP' | 'PKR' | 'PLN' | 'SEK' | 'SGD' | 'THB' | 'TJS' | 'TRY' | 'TWD' | 'UAH' | 'VND' | 'ZAR'; //Currency of the returned prices, `USD` by default (optional) (default to undefined)

const { status, data } = await apiInstance.getPoolGroupsV1(
    currency
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **currency** | [**&#39;USD&#39; | &#39;ARS&#39; | &#39;AMD&#39; | &#39;AUD&#39; | &#39;AZN&#39; | &#39;BDT&#39; | &#39;BRL&#39; | &#39;BTC&#39; | &#39;BYN&#39; | &#39;CAD&#39; | &#39;CHF&#39; | &#39;CLP&#39; | &#39;CNY&#39; | &#39;COP&#39; | &#39;CZK&#39; | &#39;DKK&#39; | &#39;EGP&#39; | &#39;EUR&#39; | &#39;GBP&#39; | &#39;GEL&#39; | &#39;HKD&#39; | &#39;HRK&#39; | &#39;HUF&#39; | &#39;IDR&#39; | &#39;ILS&#39; | &#39;INR&#39; | &#39;JPY&#39; | &#39;KGS&#39; | &#39;KRW&#39; | &#39;KZT&#39; | &#39;MAD&#39; | &#39;MXN&#39; | &#39;MYR&#39; | &#39;NGN&#39; | &#39;NOK&#39; | &#39;NZD&#39; | &#39;PEN&#39; | &#39;PHP&#39; | &#39;PKR&#39; | &#39;PLN&#39; | &#39;SEK&#39; | &#39;SGD&#39; | &#39;THB&#39; | &#39;TJS&#39; | &#39;TRY&#39; | &#39;TWD&#39; | &#39;UAH&#39; | &#39;VND&#39; | &#39;ZAR&#39;**]**Array<&#39;USD&#39; &#124; &#39;ARS&#39; &#124; &#39;AMD&#39; &#124; &#39;AUD&#39; &#124; &#39;AZN&#39; &#124; &#39;BDT&#39; &#124; &#39;BRL&#39; &#124; &#39;BTC&#39; &#124; &#39;BYN&#39; &#124; &#39;CAD&#39; &#124; &#39;CHF&#39; &#124; &#39;CLP&#39; &#124; &#39;CNY&#39; &#124; &#39;COP&#39; &#124; &#39;CZK&#39; &#124; &#39;DKK&#39; &#124; &#39;EGP&#39; &#124; &#39;EUR&#39; &#124; &#39;GBP&#39; &#124; &#39;GEL&#39; &#124; &#39;HKD&#39; &#124; &#39;HRK&#39; &#124; &#39;HUF&#39; &#124; &#39;IDR&#39; &#124; &#39;ILS&#39; &#124; &#39;INR&#39; &#124; &#39;JPY&#39; &#124; &#39;KGS&#39; &#124; &#39;KRW&#39; &#124; &#39;KZT&#39; &#124; &#39;MAD&#39; &#124; &#39;MXN&#39; &#124; &#39;MYR&#39; &#124; &#39;NGN&#39; &#124; &#39;NOK&#39; &#124; &#39;NZD&#39; &#124; &#39;PEN&#39; &#124; &#39;PHP&#39; &#124; &#39;PKR&#39; &#124; &#39;PLN&#39; &#124; &#39;SEK&#39; &#124; &#39;SGD&#39; &#124; &#39;THB&#39; &#124; &#39;TJS&#39; &#124; &#39;TRY&#39; &#124; &#39;TWD&#39; &#124; &#39;UAH&#39; &#124; &#39;VND&#39; &#124; &#39;ZAR&#39;>** | Currency of the returned prices, &#x60;USD&#x60; by default | (optional) defaults to undefined|


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
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

