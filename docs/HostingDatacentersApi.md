# HostingDatacentersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listAvailableDatacentersV1**](#listavailabledatacentersv1) | **GET** /api/hosting/v1/datacenters | List available datacenters|

# **listAvailableDatacentersV1**
> Array<HostingV1DatacenterDatacenterResource> listAvailableDatacentersV1()

Retrieve a list of datacenters available for setting up hosting plans based on available datacenter capacity and hosting plan of your order. The first item in the list is the best match for your specific order requirements.

### Example

```typescript
import {
    HostingDatacentersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatacentersApi(configuration);

let orderId: number; //Order ID (default to undefined)

const { status, data } = await apiInstance.listAvailableDatacentersV1(
    orderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Order ID | defaults to undefined|


### Return type

**Array<HostingV1DatacenterDatacenterResource>**

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

