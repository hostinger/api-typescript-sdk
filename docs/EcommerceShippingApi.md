# EcommerceShippingApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**setStoreShippingV1**](#setstoreshippingv1) | **POST** /api/ecommerce/v1/stores/{store_id}/shipping | Set store shipping|

# **setStoreShippingV1**
> EcommerceV1ShippingShippingResource setStoreShippingV1(ecommerceV1ShippingSetShippingRequest)

Set the flat-rate shipping price for a store, creating the shipping zone if it does not exist yet.

### Example

```typescript
import {
    EcommerceShippingApi,
    Configuration,
    EcommerceV1ShippingSetShippingRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceShippingApi(configuration);

let storeId: string; //The ID of the store to configure shipping for. (default to undefined)
let ecommerceV1ShippingSetShippingRequest: EcommerceV1ShippingSetShippingRequest; //

const { status, data } = await apiInstance.setStoreShippingV1(
    storeId,
    ecommerceV1ShippingSetShippingRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1ShippingSetShippingRequest** | **EcommerceV1ShippingSetShippingRequest**|  | |
| **storeId** | [**string**] | The ID of the store to configure shipping for. | defaults to undefined|


### Return type

**EcommerceV1ShippingShippingResource**

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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

