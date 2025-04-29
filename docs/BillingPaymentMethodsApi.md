# BillingPaymentMethodsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deletePaymentMethodV1**](#deletepaymentmethodv1) | **DELETE** /api/billing/v1/payment-methods/{paymentMethodId} | Delete payment method|
|[**getPaymentMethodListV1**](#getpaymentmethodlistv1) | **GET** /api/billing/v1/payment-methods | Get payment method list|
|[**setDefaultPaymentMethodV1**](#setdefaultpaymentmethodv1) | **POST** /api/billing/v1/payment-methods/{paymentMethodId} | Set default payment method|

# **deletePaymentMethodV1**
> CommonSuccessEmptyResource deletePaymentMethodV1()

This endpoint deletes a payment method from your account.

### Example

```typescript
import {
    BillingPaymentMethodsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingPaymentMethodsApi(configuration);

let paymentMethodId: number; //Payment method ID (default to undefined)

const { status, data } = await apiInstance.deletePaymentMethodV1(
    paymentMethodId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **paymentMethodId** | [**number**] | Payment method ID | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPaymentMethodListV1**
> Array<BillingV1PaymentMethodPaymentMethodResource> getPaymentMethodListV1()

This endpoint retrieves a list of available payment methods that can be used for placing new orders.  If you want to add new payment method, please use [hPanel](https://hpanel.hostinger.com/billing/payment-methods).

### Example

```typescript
import {
    BillingPaymentMethodsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingPaymentMethodsApi(configuration);

const { status, data } = await apiInstance.getPaymentMethodListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<BillingV1PaymentMethodPaymentMethodResource>**

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

# **setDefaultPaymentMethodV1**
> CommonSuccessEmptyResource setDefaultPaymentMethodV1()

This endpoint sets default payment method for your account.

### Example

```typescript
import {
    BillingPaymentMethodsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new BillingPaymentMethodsApi(configuration);

let paymentMethodId: number; //Payment method ID (default to undefined)

const { status, data } = await apiInstance.setDefaultPaymentMethodV1(
    paymentMethodId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **paymentMethodId** | [**number**] | Payment method ID | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

