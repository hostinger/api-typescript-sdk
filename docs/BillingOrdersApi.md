# BillingOrdersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createNewServiceOrderV1**](#createnewserviceorderv1) | **POST** /api/billing/v1/orders | Create new service order|

# **createNewServiceOrderV1**
> BillingV1OrderOrderResource createNewServiceOrderV1(billingV1OrderStoreRequest)

This endpoint creates a new service order.   To place order, you need to provide payment method ID and list of price items from the catalog endpoint together with quantity. Coupons also can be provided during order creation.  Orders created using this endpoint will be set for automatic renewal.  Some `credit_card` payments might need additional verification, rendering purchase unprocessed. We recommend use other payment methods than `credit_card` if you encounter this issue.

### Example

```typescript
import {
    BillingOrdersApi,
    Configuration,
    BillingV1OrderStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingOrdersApi(configuration);

let billingV1OrderStoreRequest: BillingV1OrderStoreRequest; //

const { status, data } = await apiInstance.createNewServiceOrderV1(
    billingV1OrderStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billingV1OrderStoreRequest** | **BillingV1OrderStoreRequest**|  | |


### Return type

**BillingV1OrderOrderResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

