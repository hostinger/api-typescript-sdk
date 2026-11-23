# EcommerceWebhooksApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAnEcommerceWebhookV1**](#createanecommercewebhookv1) | **POST** /api/ecommerce/v1/stores/{store_id}/webhooks | Create an ecommerce webhook|
|[**deleteAnEcommerceWebhookV1**](#deleteanecommercewebhookv1) | **DELETE** /api/ecommerce/v1/stores/{store_id}/webhooks/{endpoint_id} | Delete an ecommerce webhook|
|[**getAnEcommerceWebhookV1**](#getanecommercewebhookv1) | **GET** /api/ecommerce/v1/stores/{store_id}/webhooks/{endpoint_id} | Get an ecommerce webhook|
|[**listEcommerceWebhooksV1**](#listecommercewebhooksv1) | **GET** /api/ecommerce/v1/stores/{store_id}/webhooks | List ecommerce webhooks|
|[**rotateAnEcommerceWebhookSecretV1**](#rotateanecommercewebhooksecretv1) | **POST** /api/ecommerce/v1/stores/{store_id}/webhooks/{endpoint_id}/rotate-secret | Rotate an ecommerce webhook secret|
|[**updateAnEcommerceWebhookV1**](#updateanecommercewebhookv1) | **PATCH** /api/ecommerce/v1/stores/{store_id}/webhooks/{endpoint_id} | Update an ecommerce webhook|

# **createAnEcommerceWebhookV1**
> EcommerceV1WebhookWebhookCreationResource createAnEcommerceWebhookV1(ecommerceV1WebhookStoreRequest)

Create an enabled subscription for your store to receive ecommerce events in external automation systems. Save the whsec_ signing secret securely; it is returned once. Up to ten endpoints, including disabled endpoints, may exist per store. Deliveries follow Standard Webhooks: verify the webhook-id, webhook-timestamp and webhook-signature headers against the raw body with an official Standard Webhooks library before parsing. Events can arrive out of order or more than once; deduplicate by event id.  400: the URL is not a public destination, or webhook_sales_channel_invalid (a channel ID does not belong to this store). 409 codes: webhook_endpoint_limit_reached, webhook_store_inactive, webhook_endpoint_catalog_busy (a catalog change is in progress; retry). Errors return the upstream code in `message`, as `[Ecommerce:<code>] <reason>`.

### Example

```typescript
import {
    EcommerceWebhooksApi,
    Configuration,
    EcommerceV1WebhookStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceWebhooksApi(configuration);

let storeId: string; //ID of the store owned by your account. (default to undefined)
let ecommerceV1WebhookStoreRequest: EcommerceV1WebhookStoreRequest; //

const { status, data } = await apiInstance.createAnEcommerceWebhookV1(
    storeId,
    ecommerceV1WebhookStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1WebhookStoreRequest** | **EcommerceV1WebhookStoreRequest**|  | |
| **storeId** | [**string**] | ID of the store owned by your account. | defaults to undefined|


### Return type

**EcommerceV1WebhookWebhookCreationResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created response |  -  |
|**400** | Error response |  -  |
|**401** | Unauthenticated response |  -  |
|**409** | Conflict response. &#x60;Retry-After&#x60;, when present, is the number of seconds to wait before retrying. |  * Retry-After - Seconds to wait before retrying the request <br>  |
|**422** | Validation error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAnEcommerceWebhookV1**
> CommonSuccessEmptyResource deleteAnEcommerceWebhookV1()

Delete a subscription owned by your store, retaining delivery audit records.

### Example

```typescript
import {
    EcommerceWebhooksApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceWebhooksApi(configuration);

let storeId: string; //ID of the store owned by your account. (default to undefined)
let endpointId: string; //Webhook endpoint ID belonging to this store. (default to undefined)

const { status, data } = await apiInstance.deleteAnEcommerceWebhookV1(
    storeId,
    endpointId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | ID of the store owned by your account. | defaults to undefined|
| **endpointId** | [**string**] | Webhook endpoint ID belonging to this store. | defaults to undefined|


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
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getAnEcommerceWebhookV1**
> EcommerceV1WebhookWebhookResource getAnEcommerceWebhookV1()

Get a subscription owned by your store, without signing secrets.

### Example

```typescript
import {
    EcommerceWebhooksApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceWebhooksApi(configuration);

let storeId: string; //ID of the store owned by your account. (default to undefined)
let endpointId: string; //Webhook endpoint ID belonging to this store. (default to undefined)

const { status, data } = await apiInstance.getAnEcommerceWebhookV1(
    storeId,
    endpointId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | ID of the store owned by your account. | defaults to undefined|
| **endpointId** | [**string**] | Webhook endpoint ID belonging to this store. | defaults to undefined|


### Return type

**EcommerceV1WebhookWebhookResource**

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
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listEcommerceWebhooksV1**
> EcommerceV1WebhookWebhookListResource listEcommerceWebhooksV1()

List your store\'s subscriptions for external automation systems, without signing secrets.

### Example

```typescript
import {
    EcommerceWebhooksApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceWebhooksApi(configuration);

let storeId: string; //ID of the store owned by your account. (default to undefined)

const { status, data } = await apiInstance.listEcommerceWebhooksV1(
    storeId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | ID of the store owned by your account. | defaults to undefined|


### Return type

**EcommerceV1WebhookWebhookListResource**

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

# **rotateAnEcommerceWebhookSecretV1**
> EcommerceV1WebhookWebhookSecretResource rotateAnEcommerceWebhookSecretV1()

Explicitly rotate the signing secret of an enabled endpoint on an active store. Save the new secret securely. Prior secrets retain their original 24-hour overlap deadlines. Repeated calls create distinct secrets, up to five live secrets. Wait for an old secret to expire at the limit. After a lost response, explicitly rotate again; stored secrets cannot be retrieved. No daily renewal is required.  409 codes: webhook_endpoint_disabled (endpoint is disabled or revoked), webhook_store_inactive, webhook_secret_rotation_limit_reached (five live secrets). Errors return the upstream code in `message`, as `[Ecommerce:<code>] <reason>`.

### Example

```typescript
import {
    EcommerceWebhooksApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceWebhooksApi(configuration);

let storeId: string; //ID of the store owned by your account. (default to undefined)
let endpointId: string; //Webhook endpoint ID belonging to this store. (default to undefined)

const { status, data } = await apiInstance.rotateAnEcommerceWebhookSecretV1(
    storeId,
    endpointId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **storeId** | [**string**] | ID of the store owned by your account. | defaults to undefined|
| **endpointId** | [**string**] | Webhook endpoint ID belonging to this store. | defaults to undefined|


### Return type

**EcommerceV1WebhookWebhookSecretResource**

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
|**404** | Error response |  -  |
|**409** | Conflict response. &#x60;Retry-After&#x60;, when present, is the number of seconds to wait before retrying. |  * Retry-After - Seconds to wait before retrying the request <br>  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateAnEcommerceWebhookV1**
> EcommerceV1WebhookWebhookResource updateAnEcommerceWebhookV1(ecommerceV1WebhookUpdateRequest)

Change the receiver, events, channel filter or enabled state. Omitted fields are preserved; a null channel filter restores store-wide delivery. Endpoints disabled automatically after a 410 Gone (receiver_gone) or persistent delivery failures (receiver_failing) resume with enabled: true; events from the disabled period are not sent. Lifecycle-revoked endpoints cannot be enabled again: delete them and create fresh subscriptions after recovery.  400 codes: webhook_destination_not_allowed (the new URL, or the saved URL when enabling, is not a public destination), webhook_sales_channel_invalid. 409 codes: webhook_endpoint_revoked, webhook_store_inactive, webhook_endpoint_catalog_busy (retry). Errors return the upstream code in `message`, as `[Ecommerce:<code>] <reason>`.

### Example

```typescript
import {
    EcommerceWebhooksApi,
    Configuration,
    EcommerceV1WebhookUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new EcommerceWebhooksApi(configuration);

let storeId: string; //ID of the store owned by your account. (default to undefined)
let endpointId: string; //Webhook endpoint ID belonging to this store. (default to undefined)
let ecommerceV1WebhookUpdateRequest: EcommerceV1WebhookUpdateRequest; //

const { status, data } = await apiInstance.updateAnEcommerceWebhookV1(
    storeId,
    endpointId,
    ecommerceV1WebhookUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ecommerceV1WebhookUpdateRequest** | **EcommerceV1WebhookUpdateRequest**|  | |
| **storeId** | [**string**] | ID of the store owned by your account. | defaults to undefined|
| **endpointId** | [**string**] | Webhook endpoint ID belonging to this store. | defaults to undefined|


### Return type

**EcommerceV1WebhookWebhookResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**400** | Error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**409** | Conflict response. &#x60;Retry-After&#x60;, when present, is the number of seconds to wait before retrying. |  * Retry-After - Seconds to wait before retrying the request <br>  |
|**422** | Validation error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

