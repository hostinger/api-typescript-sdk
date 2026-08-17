# AgencyHostingMetricsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listAgencyPlanOrderDiskUsageMetricsV1**](#listagencyplanorderdiskusagemetricsv1) | **GET** /api/agency-hosting/v1/orders/{order_id}/disk-usage-metrics | List Agency Plan order disk usage metrics|
|[**listOrderResourceUsageMetricsV1**](#listorderresourceusagemetricsv1) | **GET** /api/agency-hosting/v1/orders/{order_id}/resource-usage-metrics | List order resource usage metrics|

# **listAgencyPlanOrderDiskUsageMetricsV1**
> AgencyHostingV1OrdersDiskUsageMetricsMetricsResource listAgencyPlanOrderDiskUsageMetricsV1()

Returns aggregated disk and inode usage for the Agency Plan order over the selected time frame, plus the plan quotas. Figures cover the whole order account. Values may be up to one hour stale. CPU, memory, and process usage are on the resource-usage-metrics endpoint.

### Example

```typescript
import {
    AgencyHostingMetricsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingMetricsApi(configuration);

let orderId: number; //Agency Plan order ID (default to undefined)
let timeFrameDays: 1 | 7 | 14 | 30; //Length of the window in days, ending now. Bucket size grows with the window. (optional) (default to 1)

const { status, data } = await apiInstance.listAgencyPlanOrderDiskUsageMetricsV1(
    orderId,
    timeFrameDays
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Agency Plan order ID | defaults to undefined|
| **timeFrameDays** | [**1 | 7 | 14 | 30**]**Array<1 &#124; 7 &#124; 14 &#124; 30>** | Length of the window in days, ending now. Bucket size grows with the window. | (optional) defaults to 1|


### Return type

**AgencyHostingV1OrdersDiskUsageMetricsMetricsResource**

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

# **listOrderResourceUsageMetricsV1**
> AgencyHostingV1OrdersResourceUsageMetricsMetricsResource listOrderResourceUsageMetricsV1()

Returns aggregated CPU, memory, and process usage for the Agency Plan order over the selected time frame, plus the plan quotas and a per-website breakdown. Each website is identified by uid. Suspended and deleted websites are excluded from both the order totals and the per-website breakdown. Values may be up to one hour stale. Disk and inode usage are on the disk-usage-metrics endpoint.

### Example

```typescript
import {
    AgencyHostingMetricsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingMetricsApi(configuration);

let orderId: number; //Agency Plan order ID (default to undefined)
let timeFrameHours: 1 | 24 | 168 | 336 | 720; //Length of the window in hours, ending now. Bucket size grows with the window. (optional) (default to 24)

const { status, data } = await apiInstance.listOrderResourceUsageMetricsV1(
    orderId,
    timeFrameHours
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Agency Plan order ID | defaults to undefined|
| **timeFrameHours** | [**1 | 24 | 168 | 336 | 720**]**Array<1 &#124; 24 &#124; 168 &#124; 336 &#124; 720>** | Length of the window in hours, ending now. Bucket size grows with the window. | (optional) defaults to 24|


### Return type

**AgencyHostingV1OrdersResourceUsageMetricsMetricsResource**

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

