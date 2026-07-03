# EcommerceSalesChannelsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createCustomSalesChannelV1**](#createcustomsaleschannelv1) | **POST** /api/ecommerce/v1/stores/{store_id}/sales-channels | Create custom sales channel|
|[**listSalesChannelsV1**](#listsaleschannelsv1) | **GET** /api/ecommerce/v1/stores/{store_id}/sales-channels | List sales channels|
|[**updateSalesChannelV1**](#updatesaleschannelv1) | **PATCH** /api/ecommerce/v1/stores/{store_id}/sales-channels/{sales_channel_id} | Update sales channel|

# **createCustomSalesChannelV1**
> EcommerceV1SalesChannelSalesChannelCreationResource createCustomSalesChannelV1(ecommerceV1SalesChannelStoreRequest)

Create a custom sales channel for a store. Build your own frontend and keep your catalog, orders, shipping and payments in sync through the Ecommerce API.

### Example

```typescript
import {
    EcommerceSalesChannelsApi,
    Configuration,
    EcommerceV1SalesChannelStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceSalesChannelsApi(configuration);

let storeId: string; //The ID of the store to create the sales channel for. (default to undefined)
let ecommerceV1SalesChannelStoreRequest: EcommerceV1SalesChannelStoreRequest; //

const { status, data } = await apiInstance.createCustomSalesChannelV1(
    storeId,
    ecommerceV1SalesChannelStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1SalesChannelStoreRequest** | **EcommerceV1SalesChannelStoreRequest**|  | |
| **storeId** | [**string**] | The ID of the store to create the sales channel for. | defaults to undefined|


### Return type

**EcommerceV1SalesChannelSalesChannelCreationResource**

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

# **listSalesChannelsV1**
> EcommerceV1SalesChannelSalesChannelListResource listSalesChannelsV1()

List a store\'s active sales channels with their full metadata.

### Example

```typescript
import {
    EcommerceSalesChannelsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceSalesChannelsApi(configuration);

let storeId: string; //The ID of the store to list sales channels for. (default to undefined)

const { status, data } = await apiInstance.listSalesChannelsV1(
    storeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to list sales channels for. | defaults to undefined|


### Return type

**EcommerceV1SalesChannelSalesChannelListResource**

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

# **updateSalesChannelV1**
> EcommerceV1SalesChannelSalesChannelUpdateResource updateSalesChannelV1(ecommerceV1SalesChannelUpdateRequest)

Update a custom sales channel. The merchant-facing `name` and the public `url` (returned as the channel `domain`) can be changed. Pass `null` to clear a value.

### Example

```typescript
import {
    EcommerceSalesChannelsApi,
    Configuration,
    EcommerceV1SalesChannelUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceSalesChannelsApi(configuration);

let storeId: string; //The ID of the store that owns the sales channel. (default to undefined)
let salesChannelId: string; //The ID of the sales channel to update. (default to undefined)
let ecommerceV1SalesChannelUpdateRequest: EcommerceV1SalesChannelUpdateRequest; //

const { status, data } = await apiInstance.updateSalesChannelV1(
    storeId,
    salesChannelId,
    ecommerceV1SalesChannelUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1SalesChannelUpdateRequest** | **EcommerceV1SalesChannelUpdateRequest**|  | |
| **storeId** | [**string**] | The ID of the store that owns the sales channel. | defaults to undefined|
| **salesChannelId** | [**string**] | The ID of the sales channel to update. | defaults to undefined|


### Return type

**EcommerceV1SalesChannelSalesChannelUpdateResource**

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

