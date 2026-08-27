# EcommerceOrdersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**cancelAnOrderV1**](#cancelanorderv1) | **POST** /api/ecommerce/v1/stores/{store_id}/orders/{order_id}/cancel | Cancel an order|
|[**fulfilAnOrderV1**](#fulfilanorderv1) | **POST** /api/ecommerce/v1/stores/{store_id}/orders/{order_id}/fulfill | Fulfil an order|
|[**listStoreOrdersV1**](#liststoreordersv1) | **GET** /api/ecommerce/v1/stores/{store_id}/orders | List store orders|
|[**retrieveAnOrderV1**](#retrieveanorderv1) | **GET** /api/ecommerce/v1/stores/{store_id}/orders/{order_id} | Retrieve an order|

# **cancelAnOrderV1**
> EcommerceV1OrderOrderResponseResource cancelAnOrderV1(ecommerceV1OrderCancelRequest)

Cancel the order and optionally email the customer. Returns the updated order summary.

### Example

```typescript
import {
    EcommerceOrdersApi,
    Configuration,
    EcommerceV1OrderCancelRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceOrdersApi(configuration);

let storeId: string; //The ID of the store that owns the order. (default to undefined)
let orderId: string; //The ID of the order to cancel. (default to undefined)
let ecommerceV1OrderCancelRequest: EcommerceV1OrderCancelRequest; //

const { status, data } = await apiInstance.cancelAnOrderV1(
    storeId,
    orderId,
    ecommerceV1OrderCancelRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1OrderCancelRequest** | **EcommerceV1OrderCancelRequest**|  | |
| **storeId** | [**string**] | The ID of the store that owns the order. | defaults to undefined|
| **orderId** | [**string**] | The ID of the order to cancel. | defaults to undefined|


### Return type

**EcommerceV1OrderOrderResponseResource**

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

# **fulfilAnOrderV1**
> EcommerceV1OrderOrderResponseResource fulfilAnOrderV1(ecommerceV1OrderFulfillRequest)

Create a fulfilment for the order and attach tracking in one call. Omit items to fulfil every remaining unfulfilled item. Returns the updated order summary.

### Example

```typescript
import {
    EcommerceOrdersApi,
    Configuration,
    EcommerceV1OrderFulfillRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceOrdersApi(configuration);

let storeId: string; //The ID of the store that owns the order. (default to undefined)
let orderId: string; //The ID of the order to fulfil. (default to undefined)
let ecommerceV1OrderFulfillRequest: EcommerceV1OrderFulfillRequest; //

const { status, data } = await apiInstance.fulfilAnOrderV1(
    storeId,
    orderId,
    ecommerceV1OrderFulfillRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1OrderFulfillRequest** | **EcommerceV1OrderFulfillRequest**|  | |
| **storeId** | [**string**] | The ID of the store that owns the order. | defaults to undefined|
| **orderId** | [**string**] | The ID of the order to fulfil. | defaults to undefined|


### Return type

**EcommerceV1OrderOrderResponseResource**

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

# **listStoreOrdersV1**
> EcommerceListStoreOrdersV1200Response listStoreOrdersV1()

List a store\'s orders newest first as summaries. Filter by status, payment or fulfilment status, customer email, order number or a free-text query. Amounts are in the smallest currency unit. Retrieve a single order for its line items, addresses and fulfilments.

### Example

```typescript
import {
    EcommerceOrdersApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceOrdersApi(configuration);

let storeId: string; //The ID of the store to list orders for. (default to undefined)
let status: Array<'pending' | 'completed' | 'archived' | 'canceled' | 'requires_action'>; //Order statuses to include. (optional) (default to undefined)
let paymentStatus: Array<'not_paid' | 'awaiting' | 'captured' | 'partially_refunded' | 'refunded' | 'canceled' | 'requires_action' | 'not_required'>; //Payment statuses to include. A paid order is \"captured\". (optional) (default to undefined)
let fulfillmentStatus: Array<'not_fulfilled' | 'partially_fulfilled' | 'fulfilled' | 'partially_shipped' | 'shipped' | 'partially_returned' | 'returned' | 'canceled' | 'requires_action'>; //Fulfilment statuses to include. (optional) (default to undefined)
let email: string; //Customer email, matched exactly. (optional) (default to undefined)
let displayId: string; //The order number the merchant and customer see. (optional) (default to undefined)
let q: string; //Free-text search over customer name, email, order number and line items. (optional) (default to undefined)
let createdAtFrom: string; //Earliest creation time to include, inclusive. Accepts a date or ISO date-time (UTC). (optional) (default to undefined)
let createdAtTo: string; //Latest creation time to include, inclusive. A bare date covers that whole day. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.listStoreOrdersV1(
    storeId,
    status,
    paymentStatus,
    fulfillmentStatus,
    email,
    displayId,
    q,
    createdAtFrom,
    createdAtTo,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store to list orders for. | defaults to undefined|
| **status** | **Array<&#39;pending&#39; &#124; &#39;completed&#39; &#124; &#39;archived&#39; &#124; &#39;canceled&#39; &#124; &#39;requires_action&#39;>** | Order statuses to include. | (optional) defaults to undefined|
| **paymentStatus** | **Array<&#39;not_paid&#39; &#124; &#39;awaiting&#39; &#124; &#39;captured&#39; &#124; &#39;partially_refunded&#39; &#124; &#39;refunded&#39; &#124; &#39;canceled&#39; &#124; &#39;requires_action&#39; &#124; &#39;not_required&#39;>** | Payment statuses to include. A paid order is \&quot;captured\&quot;. | (optional) defaults to undefined|
| **fulfillmentStatus** | **Array<&#39;not_fulfilled&#39; &#124; &#39;partially_fulfilled&#39; &#124; &#39;fulfilled&#39; &#124; &#39;partially_shipped&#39; &#124; &#39;shipped&#39; &#124; &#39;partially_returned&#39; &#124; &#39;returned&#39; &#124; &#39;canceled&#39; &#124; &#39;requires_action&#39;>** | Fulfilment statuses to include. | (optional) defaults to undefined|
| **email** | [**string**] | Customer email, matched exactly. | (optional) defaults to undefined|
| **displayId** | [**string**] | The order number the merchant and customer see. | (optional) defaults to undefined|
| **q** | [**string**] | Free-text search over customer name, email, order number and line items. | (optional) defaults to undefined|
| **createdAtFrom** | [**string**] | Earliest creation time to include, inclusive. Accepts a date or ISO date-time (UTC). | (optional) defaults to undefined|
| **createdAtTo** | [**string**] | Latest creation time to include, inclusive. A bare date covers that whole day. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**EcommerceListStoreOrdersV1200Response**

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

# **retrieveAnOrderV1**
> EcommerceV1OrderOrderDetailResponseResource retrieveAnOrderV1()

Retrieve one order in full: line items (each with the id the fulfil endpoint needs), addresses, the totals breakdown and fulfilments with tracking. Amounts are in the smallest currency unit.

### Example

```typescript
import {
    EcommerceOrdersApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceOrdersApi(configuration);

let storeId: string; //The ID of the store that owns the order. (default to undefined)
let orderId: string; //The ID of the order to retrieve. (default to undefined)

const { status, data } = await apiInstance.retrieveAnOrderV1(
    storeId,
    orderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | The ID of the store that owns the order. | defaults to undefined|
| **orderId** | [**string**] | The ID of the order to retrieve. | defaults to undefined|


### Return type

**EcommerceV1OrderOrderDetailResponseResource**

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

