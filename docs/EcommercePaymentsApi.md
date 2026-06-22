# EcommercePaymentsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**enableManualPaymentMethodV1**](#enablemanualpaymentmethodv1) | **POST** /api/ecommerce/v1/stores/{store_id}/payment-methods/manual | Enable manual payment method|

# **enableManualPaymentMethodV1**
> EcommerceV1PaymentManualPaymentResource enableManualPaymentMethodV1(ecommerceV1PaymentEnableManualPaymentRequest)

Enable a manual payment method so the store can accept orders without an online payment provider.

### Example

```typescript
import {
    EcommercePaymentsApi,
    Configuration,
    EcommerceV1PaymentEnableManualPaymentRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommercePaymentsApi(configuration);

let storeId: string; //The ID of the store to enable manual payment for. (default to undefined)
let ecommerceV1PaymentEnableManualPaymentRequest: EcommerceV1PaymentEnableManualPaymentRequest; //

const { status, data } = await apiInstance.enableManualPaymentMethodV1(
    storeId,
    ecommerceV1PaymentEnableManualPaymentRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1PaymentEnableManualPaymentRequest** | **EcommerceV1PaymentEnableManualPaymentRequest**|  | |
| **storeId** | [**string**] | The ID of the store to enable manual payment for. | defaults to undefined|


### Return type

**EcommerceV1PaymentManualPaymentResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

