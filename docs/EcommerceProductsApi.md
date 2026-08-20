# EcommerceProductsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAProductImageUploadURLV1**](#createaproductimageuploadurlv1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/{product_id}/images/upload-url | Create a product image upload URL|
|[**createDigitalProductV1**](#createdigitalproductv1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/digital | Create digital product|
|[**createPhysicalProductV1**](#createphysicalproductv1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/physical | Create physical product|
|[**deleteAProductV1**](#deleteaproductv1) | **DELETE** /api/ecommerce/v1/stores/{store_id}/products/{product_id} | Delete a product|
|[**listProductsV1**](#listproductsv1) | **GET** /api/ecommerce/v1/stores/{store_id}/products | List products|
|[**updateAProductV1**](#updateaproductv1) | **PATCH** /api/ecommerce/v1/stores/{store_id}/products/{product_id} | Update a product|
|[**uploadAndAttachAProductImageV1**](#uploadandattachaproductimagev1) | **POST** /api/ecommerce/v1/stores/{store_id}/products/{product_id}/images | Upload and attach a product image|

# **createAProductImageUploadURLV1**
> EcommerceV1ProductProductImageUploadUrlResource createAProductImageUploadURLV1()

Returns a signed URL to upload a product image to (multipart/form-data POST). Then call the attach-image endpoint with the returned object_name to scan and attach it to the product.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store the product belongs to. (default to undefined)
let productId: string; //The ID of the product the image will be attached to. (default to undefined)

const { status, data } = await apiInstance.createAProductImageUploadURLV1(
    storeId,
    productId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store the product belongs to. | defaults to undefined|
| **productId** | [**string**] | The ID of the product the image will be attached to. | defaults to undefined|


### Return type

**EcommerceV1ProductProductImageUploadUrlResource**

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

# **deleteAProductV1**
> EcommerceV1ProductProductDeletedResource deleteAProductV1()

Delete a product and its variants from the store. A subscription product with active subscribers is archived instead of deleted so its data stays available.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store that owns the product. (default to undefined)
let productId: string; //The ID of the product to delete. (default to undefined)

const { status, data } = await apiInstance.deleteAProductV1(
    storeId,
    productId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store that owns the product. | defaults to undefined|
| **productId** | [**string**] | The ID of the product to delete. | defaults to undefined|


### Return type

**EcommerceV1ProductProductDeletedResource**

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

# **listProductsV1**
> EcommerceListProductsV1200Response listProductsV1()

List a store\'s products newest first as lean summaries (name, status, thumbnail, variant count and price range). Prices are integers in the smallest currency unit and live on variants. Filter by status, free text or a set of product ids. Use include=variants to embed each product\'s variants with prices and inventory, and include=media to embed its media.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store to list products for. (default to undefined)
let productIds: Array<string>; //Restrict to these product ids. Doubles as a single-product lookup. Up to 200 ids. (optional) (default to undefined)
let status: Array<'draft' | 'proposed' | 'published' | 'rejected' | 'archived'>; //Product statuses to include. (optional) (default to undefined)
let q: string; //Free-text search over product title and SKU. (optional) (default to undefined)
let include: Array<'variants' | 'media'>; //Opt-in heavy data: \"variants\" embeds each product\'s variants; \"media\" embeds its media. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.listProductsV1(
    storeId,
    productIds,
    status,
    q,
    include,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to list products for. | defaults to undefined|
| **productIds** | **Array&lt;string&gt;** | Restrict to these product ids. Doubles as a single-product lookup. Up to 200 ids. | (optional) defaults to undefined|
| **status** | **Array<&#39;draft&#39; &#124; &#39;proposed&#39; &#124; &#39;published&#39; &#124; &#39;rejected&#39; &#124; &#39;archived&#39;>** | Product statuses to include. | (optional) defaults to undefined|
| **q** | [**string**] | Free-text search over product title and SKU. | (optional) defaults to undefined|
| **include** | **Array<&#39;variants&#39; &#124; &#39;media&#39;>** | Opt-in heavy data: \&quot;variants\&quot; embeds each product\&#39;s variants; \&quot;media\&quot; embeds its media. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**EcommerceListProductsV1200Response**

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

# **updateAProductV1**
> EcommerceV1ProductProductResponseResource updateAProductV1(ecommerceV1ProductUpdateRequest)

Update a product\'s name, description or status. Set status to published to make it buyable, draft to hide it, or archived to retire it. Variants, prices and inventory are managed through the variant endpoints, not here. Returns the updated product summary.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration,
    EcommerceV1ProductUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store that owns the product. (default to undefined)
let productId: string; //The ID of the product to update. (default to undefined)
let ecommerceV1ProductUpdateRequest: EcommerceV1ProductUpdateRequest; //

const { status, data } = await apiInstance.updateAProductV1(
    storeId,
    productId,
    ecommerceV1ProductUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1ProductUpdateRequest** | **EcommerceV1ProductUpdateRequest**|  | |
| **storeId** | [**string**] | The ID of the store that owns the product. | defaults to undefined|
| **productId** | [**string**] | The ID of the product to update. | defaults to undefined|


### Return type

**EcommerceV1ProductProductResponseResource**

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

# **uploadAndAttachAProductImageV1**
> EcommerceV1ProductProductImageUploadResource uploadAndAttachAProductImageV1(ecommerceV1ProductUploadProductImageRequest)

Fetch a raster image (JPEG, PNG, GIF or WebP, max 15MB) from a URL and attach it to a product in a single call. The image is virus-scanned and validated by content, then stored on the CDN. Set is_thumbnail to make it the product\'s primary image.

### Example

```typescript
import {
    EcommerceProductsApi,
    Configuration,
    EcommerceV1ProductUploadProductImageRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceProductsApi(configuration);

let storeId: string; //The ID of the store the product belongs to. (default to undefined)
let productId: string; //The ID of the product to attach the image to. (default to undefined)
let ecommerceV1ProductUploadProductImageRequest: EcommerceV1ProductUploadProductImageRequest; //

const { status, data } = await apiInstance.uploadAndAttachAProductImageV1(
    storeId,
    productId,
    ecommerceV1ProductUploadProductImageRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1ProductUploadProductImageRequest** | **EcommerceV1ProductUploadProductImageRequest**|  | |
| **storeId** | [**string**] | The ID of the store the product belongs to. | defaults to undefined|
| **productId** | [**string**] | The ID of the product to attach the image to. | defaults to undefined|


### Return type

**EcommerceV1ProductProductImageUploadResource**

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

