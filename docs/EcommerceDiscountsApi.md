# EcommerceDiscountsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createADiscountV1**](#createadiscountv1) | **POST** /api/ecommerce/v1/stores/{store_id}/discounts | Create a discount|
|[**listDiscountsV1**](#listdiscountsv1) | **GET** /api/ecommerce/v1/stores/{store_id}/discounts | List discounts|

# **createADiscountV1**
> EcommerceV1DiscountDiscountResponseResource createADiscountV1(ecommerceV1DiscountCreateDiscountRequest)

Create a discount for a store. Fixed discounts take an amount in the smallest currency unit (e.g. $10 is 1000); percentage discounts take a whole-number value between 1 and 100. Free-shipping discounts ignore value. Returns the created discount.

### Example

```typescript
import {
    EcommerceDiscountsApi,
    Configuration,
    EcommerceV1DiscountCreateDiscountRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceDiscountsApi(configuration);

let storeId: string; //The ID of the store to create the discount for. (default to undefined)
let ecommerceV1DiscountCreateDiscountRequest: EcommerceV1DiscountCreateDiscountRequest; //

const { status, data } = await apiInstance.createADiscountV1(
    storeId,
    ecommerceV1DiscountCreateDiscountRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1DiscountCreateDiscountRequest** | **EcommerceV1DiscountCreateDiscountRequest**|  | |
| **storeId** | [**string**] | The ID of the store to create the discount for. | defaults to undefined|


### Return type

**EcommerceV1DiscountDiscountResponseResource**

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

# **listDiscountsV1**
> EcommerceListDiscountsV1200Response listDiscountsV1()

List a store\'s discounts. Filter by free text over code and name, or by disabled state. Amounts for fixed discounts are integers in the smallest currency unit; percentage discounts carry a whole-number value between 1 and 100.

### Example

```typescript
import {
    EcommerceDiscountsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceDiscountsApi(configuration);

let storeId: string; //The ID of the store to list discounts for. (default to undefined)
let q: string; //Free-text search over discount code and name. (optional) (default to undefined)
let isDisabled: 'true' | 'false'; //Filter by disabled state. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.listDiscountsV1(
    storeId,
    q,
    isDisabled,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to list discounts for. | defaults to undefined|
| **q** | [**string**] | Free-text search over discount code and name. | (optional) defaults to undefined|
| **isDisabled** | [**&#39;true&#39; | &#39;false&#39;**]**Array<&#39;true&#39; &#124; &#39;false&#39;>** | Filter by disabled state. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**EcommerceListDiscountsV1200Response**

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

