# EcommerceProductsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createDigitalProductV1**](#createdigitalproductv1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/digital | Create digital product|
|[**createPhysicalProductV1**](#createphysicalproductv1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/physical | Create physical product|

# **createDigitalProductV1**
> EcommerceV1ProductProductCreationResource createDigitalProductV1(ecommerceV1ProductCreateDigitalProductRequest)

Create a published digital product with a single variant and an optional external download link.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration,
    EcommerceV1ProductCreateDigitalProductRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store to create the product in. (default to undefined)
let ecommerceV1ProductCreateDigitalProductRequest: EcommerceV1ProductCreateDigitalProductRequest; //

const { status, data } = await apiInstance.createDigitalProductV1(
    storeId,
    ecommerceV1ProductCreateDigitalProductRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1ProductCreateDigitalProductRequest** | **EcommerceV1ProductCreateDigitalProductRequest**|  | |
| **storeId** | [**string**] | The ID of the store to create the product in. | defaults to undefined|


### Return type

**EcommerceV1ProductProductCreationResource**

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

# **createPhysicalProductV1**
> EcommerceV1ProductProductCreationResource createPhysicalProductV1(ecommerceV1ProductCreatePhysicalProductRequest)

Create a published physical product with a single variant priced in the store currency.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration,
    EcommerceV1ProductCreatePhysicalProductRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store to create the product in. (default to undefined)
let ecommerceV1ProductCreatePhysicalProductRequest: EcommerceV1ProductCreatePhysicalProductRequest; //

const { status, data } = await apiInstance.createPhysicalProductV1(
    storeId,
    ecommerceV1ProductCreatePhysicalProductRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1ProductCreatePhysicalProductRequest** | **EcommerceV1ProductCreatePhysicalProductRequest**|  | |
| **storeId** | [**string**] | The ID of the store to create the product in. | defaults to undefined|


### Return type

**EcommerceV1ProductProductCreationResource**

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

