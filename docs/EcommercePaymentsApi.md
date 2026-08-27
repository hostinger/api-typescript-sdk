# EcommercePaymentsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAPaymentProviderConnectLinkV1**](#createapaymentproviderconnectlinkv1) | **POST** /api/ecommerce/v1/stores/{store_id}/payment-providers/{provider_id}/connect-link | Create a payment provider connect link|
|[**enableManualPaymentMethodV1**](#enablemanualpaymentmethodv1) | **POST** /api/ecommerce/v1/stores/{store_id}/payment-methods/manual | Enable manual payment method|
|[**listStorePaymentProvidersV1**](#liststorepaymentprovidersv1) | **GET** /api/ecommerce/v1/stores/{store_id}/payment-providers | List store payment providers|

# **createAPaymentProviderConnectLinkV1**
> EcommerceV1PaymentProviderPaymentProviderConnectLinkResource createAPaymentProviderConnectLinkV1()

Create an onboarding link for connecting a payment gateway to the store. Returns the gateway onboarding URL for the merchant to open and a deep-link into the store admin.

### Example

```typescript
import {
    EcommercePaymentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommercePaymentsApi(configuration);

let storeId: string; //The ID of the store to connect the payment provider to. (default to undefined)
let providerId: string; //The ID of the payment gateway to connect, e.g. stripe. (default to undefined)

const { status, data } = await apiInstance.createAPaymentProviderConnectLinkV1(
    storeId,
    providerId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to connect the payment provider to. | defaults to undefined|
| **providerId** | [**string**] | The ID of the payment gateway to connect, e.g. stripe. | defaults to undefined|


### Return type

**EcommerceV1PaymentProviderPaymentProviderConnectLinkResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableManualPaymentMethodV1**
> EcommerceV1PaymentManualPaymentResource enableManualPaymentMethodV1(ecommerceV1PaymentEnableManualPaymentRequest)

Enable a manual payment method so the store can accept orders without an online payment provider.

### Example

```typescript
import {
    EcommercePaymentsApi,
    Configuration,
    EcommerceV1PaymentEnableManualPaymentRequest
} from '@hostinger/sdk';

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

# **listStorePaymentProvidersV1**
> EcommerceV1PaymentProviderPaymentProviderListResource listStorePaymentProvidersV1()

List a store\'s payment providers, split into providers already connected to the store and gateways available to install. Never exposes gateway credentials, secrets, or configuration.

### Example

```typescript
import {
    EcommercePaymentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommercePaymentsApi(configuration);

let storeId: string; //The ID of the store to list payment providers for. (default to undefined)
let includeCurrencyUnsupported: boolean; //Include gateways that do not support the store currency in the available list. (optional) (default to undefined)

const { status, data } = await apiInstance.listStorePaymentProvidersV1(
    storeId,
    includeCurrencyUnsupported
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to list payment providers for. | defaults to undefined|
| **includeCurrencyUnsupported** | [**boolean**] | Include gateways that do not support the store currency in the available list. | (optional) defaults to undefined|


### Return type

**EcommerceV1PaymentProviderPaymentProviderListResource**

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

