# EcommerceStoresApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createStoreV1**](#createstorev1) | **POST** /api/ecommerce/v1/stores | Create store|
|[**deleteStoreV1**](#deletestorev1) | **DELETE** /api/ecommerce/v1/stores/{store_id} | Delete store|
|[**getStoresV1**](#getstoresv1) | **GET** /api/ecommerce/v1/stores | Get stores|

# **createStoreV1**
> EcommerceV1StoreStoreCreationResource createStoreV1(ecommerceV1StoreStoreRequest)

Create a new store for your account.  A primary sales channel is created alongside the store.

### Example

```typescript
import {
    EcommerceStoresApi,
    Configuration,
    EcommerceV1StoreStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceStoresApi(configuration);

let ecommerceV1StoreStoreRequest: EcommerceV1StoreStoreRequest; //

const { status, data } = await apiInstance.createStoreV1(
    ecommerceV1StoreStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1StoreStoreRequest** | **EcommerceV1StoreStoreRequest**|  | |


### Return type

**EcommerceV1StoreStoreCreationResource**

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

# **deleteStoreV1**
> EcommerceV1StoreStoreDeleteResource deleteStoreV1()

Soft-delete a store owned by your account.  The underlying store data is preserved; only the store is marked as deleted.

### Example

```typescript
import {
    EcommerceStoresApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceStoresApi(configuration);

let storeId: string; //The ID of the store to delete. (default to undefined)

const { status, data } = await apiInstance.deleteStoreV1(
    storeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to delete. | defaults to undefined|


### Return type

**EcommerceV1StoreStoreDeleteResource**

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

# **getStoresV1**
> EcommerceGetStoresV1200Response getStoresV1()

Retrieve the stores associated with your account.

### Example

```typescript
import {
    EcommerceStoresApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceStoresApi(configuration);

let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getStoresV1(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**EcommerceGetStoresV1200Response**

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

