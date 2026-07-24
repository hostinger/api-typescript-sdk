# AgencyHostingOrdersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listAgencyPlanOrdersV1**](#listagencyplanordersv1) | **GET** /api/agency-hosting/v1/orders | List Agency Plan orders|

# **listAgencyPlanOrdersV1**
> AgencyHostingListAgencyPlanOrdersV1200Response listAgencyPlanOrdersV1()

Returns a paginated list of Agency Plan orders accessible to the authenticated client.

### Example

```typescript
import {
    AgencyHostingOrdersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingOrdersApi(configuration);

let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAgencyPlanOrdersV1(
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**AgencyHostingListAgencyPlanOrdersV1200Response**

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

