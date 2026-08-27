# EcommerceProductVariantsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAProductVariantV1**](#createaproductvariantv1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/{product_id}/variants | Create a product variant|
|[**deleteAProductVariantV1**](#deleteaproductvariantv1) | **DELETE** /api/ecommerce/v1/stores/{store_id}/products/{product_id}/variants/{variant_id} | Delete a product variant|
|[**listProductVariantsV1**](#listproductvariantsv1) | **GET** /api/ecommerce/v1/stores/{store_id}/products/{product_id}/variants | List product variants|
|[**updateProductVariantsInBatchV1**](#updateproductvariantsinbatchv1) | **PATCH** /api/ecommerce/v1/stores/{store_id}/products/{product_id}/variants/batch | Update product variants in batch|

# **createAProductVariantV1**
> EcommerceV1VariantVariantResponseResource createAProductVariantV1(ecommerceV1VariantCreateVariantRequest)

Add a variant to a product along one or more option dimensions (e.g. Size, Color). Options missing from the product are created automatically; provide a value for every option the product already has. Prices are integers in the smallest currency unit and default to the store currency. Returns the created variant.

### Example

```typescript
import {
    EcommerceProductVariantsApi,
    Configuration,
    EcommerceV1VariantCreateVariantRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductVariantsApi(configuration);

let storeId: string; //The ID of the store that owns the product. (default to undefined)
let productId: string; //The ID of the product to add the variant to. (default to undefined)
let ecommerceV1VariantCreateVariantRequest: EcommerceV1VariantCreateVariantRequest; //

const { status, data } = await apiInstance.createAProductVariantV1(
    storeId,
    productId,
    ecommerceV1VariantCreateVariantRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1VariantCreateVariantRequest** | **EcommerceV1VariantCreateVariantRequest**|  | |
| **storeId** | [**string**] | The ID of the store that owns the product. | defaults to undefined|
| **productId** | [**string**] | The ID of the product to add the variant to. | defaults to undefined|


### Return type

**EcommerceV1VariantVariantResponseResource**

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

# **deleteAProductVariantV1**
> EcommerceV1VariantVariantDeletedResource deleteAProductVariantV1()

Delete a single variant from the product.

### Example

```typescript
import {
    EcommerceProductVariantsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductVariantsApi(configuration);

let storeId: string; //The ID of the store that owns the product. (default to undefined)
let productId: string; //The ID of the product that owns the variant. (default to undefined)
let variantId: string; //The ID of the variant to delete. (default to undefined)

const { status, data } = await apiInstance.deleteAProductVariantV1(
    storeId,
    productId,
    variantId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store that owns the product. | defaults to undefined|
| **productId** | [**string**] | The ID of the product that owns the variant. | defaults to undefined|
| **variantId** | [**string**] | The ID of the variant to delete. | defaults to undefined|


### Return type

**EcommerceV1VariantVariantDeletedResource**

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

# **listProductVariantsV1**
> EcommerceListProductVariantsV1200Response listProductVariantsV1()

List a product\'s variants, ordered by rank, with their options, prices and inventory. Prices are integers in the smallest currency unit and live on variants.

### Example

```typescript
import {
    EcommerceProductVariantsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductVariantsApi(configuration);

let storeId: string; //The ID of the store that owns the product. (default to undefined)
let productId: string; //The ID of the product to list variants for. (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.listProductVariantsV1(
    storeId,
    productId,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store that owns the product. | defaults to undefined|
| **productId** | [**string**] | The ID of the product to list variants for. | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**EcommerceListProductVariantsV1200Response**

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

# **updateProductVariantsInBatchV1**
> EcommerceV1VariantVariantListResponseResource updateProductVariantsInBatchV1(ecommerceV1VariantBatchUpdateVariantsRequest)

Update up to 100 existing variants in place by id — title, inventory, stock tracking and prices. Variants omitted from the request are left untouched. Prices replace the variant\'s existing prices in full. Returns the updated variants.

### Example

```typescript
import {
    EcommerceProductVariantsApi,
    Configuration,
    EcommerceV1VariantBatchUpdateVariantsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductVariantsApi(configuration);

let storeId: string; //The ID of the store that owns the product. (default to undefined)
let productId: string; //The ID of the product whose variants are being updated. (default to undefined)
let ecommerceV1VariantBatchUpdateVariantsRequest: EcommerceV1VariantBatchUpdateVariantsRequest; //

const { status, data } = await apiInstance.updateProductVariantsInBatchV1(
    storeId,
    productId,
    ecommerceV1VariantBatchUpdateVariantsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1VariantBatchUpdateVariantsRequest** | **EcommerceV1VariantBatchUpdateVariantsRequest**|  | |
| **storeId** | [**string**] | The ID of the store that owns the product. | defaults to undefined|
| **productId** | [**string**] | The ID of the product whose variants are being updated. | defaults to undefined|


### Return type

**EcommerceV1VariantVariantListResponseResource**

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

