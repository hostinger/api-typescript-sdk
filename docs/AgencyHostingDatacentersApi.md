# AgencyHostingDatacentersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listAvailableDatacentersForAnAgencyPlanOrderV1**](#listavailabledatacentersforanagencyplanorderv1) | **GET** /api/agency-hosting/v1/orders/{order_id}/datacenters | List available datacenters for an Agency Plan order|

# **listAvailableDatacentersForAnAgencyPlanOrderV1**
> Array<AgencyHostingV1DatacentersDatacenterResource> listAvailableDatacentersForAnAgencyPlanOrderV1()

Lists the datacenters available for provisioning a new website on the given Agency Plan hosting order.  Each datacenter includes a `pinger_url` you can ping from the client to measure round-trip latency; comparing the results across datacenters lets you pick the nearest one (lowest ping) before choosing its `code` as the `datacenter_code` when creating a website setup.

### Example

```typescript
import {
    AgencyHostingDatacentersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDatacentersApi(configuration);

let orderId: number; //Agency Plan order ID (default to undefined)

const { status, data } = await apiInstance.listAvailableDatacentersForAnAgencyPlanOrderV1(
    orderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Agency Plan order ID | defaults to undefined|


### Return type

**Array<AgencyHostingV1DatacentersDatacenterResource>**

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

