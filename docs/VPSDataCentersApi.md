# VPSDataCentersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getDataCentersListV1**](#getdatacenterslistv1) | **GET** /api/vps/v1/data-centers | Get data centers list|

# **getDataCentersListV1**
> Array<VPSV1DataCenterDataCenterResource> getDataCentersListV1()

This endpoint retrieves a list of all data centers available.

### Example

```typescript
import {
    VPSDataCentersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDataCentersApi(configuration);

const { status, data } = await apiInstance.getDataCentersListV1();
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

