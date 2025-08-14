# VPSDataCentersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getDataCenterListV1**](#getdatacenterlistv1) | **GET** /api/vps/v1/data-centers | Get data center list|

# **getDataCenterListV1**
> Array<VPSV1DataCenterDataCenterResource> getDataCenterListV1()

Retrieve all available data centers.  Use this endpoint to view location options before deploying VPS instances.

### Example

```typescript
import {
    VPSDataCentersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDataCentersApi(configuration);

const { status, data } = await apiInstance.getDataCenterListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<VPSV1DataCenterDataCenterResource>**

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

