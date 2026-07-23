# MailWebhooksApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebhookV1**](#createwebhookv1) | **POST** /api/mail/v1/mailboxes/{mailboxId}/webhooks | Create webhook|
|[**deleteWebhookV1**](#deletewebhookv1) | **DELETE** /api/mail/v1/webhooks/{webhookId} | Delete webhook|
|[**getWebhookV1**](#getwebhookv1) | **GET** /api/mail/v1/webhooks/{webhookId} | Get webhook|
|[**listWebhookDeliveryLogsV1**](#listwebhookdeliverylogsv1) | **GET** /api/mail/v1/orders/{orderId}/webhooks/delivery-logs | List webhook delivery logs|
|[**listWebhooksV1**](#listwebhooksv1) | **GET** /api/mail/v1/orders/{orderId}/webhooks | List webhooks|
|[**regenerateWebhookSecretV1**](#regeneratewebhooksecretv1) | **POST** /api/mail/v1/webhooks/{webhookId}/regenerate-secret | Regenerate webhook secret|
|[**testWebhookV1**](#testwebhookv1) | **POST** /api/mail/v1/webhooks/{webhookId}/test | Test webhook|
|[**updateWebhookV1**](#updatewebhookv1) | **PATCH** /api/mail/v1/webhooks/{webhookId} | Update webhook|

# **createWebhookV1**
> MailV1WebhooksWebhookCreatedResource createWebhookV1(mailV1SchemaCreateWebhookRequestSchema)

Create a webhook for the given mailbox. The generated secret is returned only in this response and is sent as a bearer token with every delivery.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration,
    MailV1SchemaCreateWebhookRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)
let mailV1SchemaCreateWebhookRequestSchema: MailV1SchemaCreateWebhookRequestSchema; //

const { status, data } = await apiInstance.createWebhookV1(
    mailboxId,
    mailV1SchemaCreateWebhookRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaCreateWebhookRequestSchema** | **MailV1SchemaCreateWebhookRequestSchema**|  | |
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


### Return type

**MailV1WebhooksWebhookCreatedResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created response |  -  |
|**401** | Unauthenticated response |  -  |
|**400** | Error response |  -  |
|**404** | Error response |  -  |
|**409** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWebhookV1**
> CommonSuccessEmptyResource deleteWebhookV1()

Permanently delete a webhook. This action cannot be undone. After deletion the URL no longer receives event notifications.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let webhookId: string; //Webhook ID (returned when the webhook was created) (default to undefined)

const { status, data } = await apiInstance.deleteWebhookV1(
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] | Webhook ID (returned when the webhook was created) | defaults to undefined|


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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWebhookV1**
> MailV1WebhooksWebhookResource getWebhookV1()

Retrieve the details of a single webhook. The webhook secret is never included; it is returned only when a webhook is created or its secret is regenerated.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let webhookId: string; //Webhook ID (returned when the webhook was created) (default to undefined)

const { status, data } = await apiInstance.getWebhookV1(
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] | Webhook ID (returned when the webhook was created) | defaults to undefined|


### Return type

**MailV1WebhooksWebhookResource**

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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWebhookDeliveryLogsV1**
> MailListWebhookDeliveryLogsV1200Response listWebhookDeliveryLogsV1()

Retrieve a paginated list of webhook delivery logs for the given mail order, including delivery outcome, duration, and retry counts. Supports filtering by mailbox.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let mailboxId: string; //Filter by the mailbox resource ID the webhooks are attached to (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listWebhookDeliveryLogsV1(
    orderId,
    mailboxId,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **mailboxId** | [**string**] | Filter by the mailbox resource ID the webhooks are attached to | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListWebhookDeliveryLogsV1200Response**

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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWebhooksV1**
> MailListWebhooksV1200Response listWebhooksV1()

Retrieve a paginated list of webhooks belonging to the given mail order. Supports filtering by mailbox and status. The webhook secret is never included; it is returned only when a webhook is created or its secret is regenerated.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let mailboxId: string; //Filter by the mailbox resource ID the webhooks are attached to (optional) (default to undefined)
let status: 'active' | 'disabled' | 'paused'; //Filter webhooks by status (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listWebhooksV1(
    orderId,
    mailboxId,
    status,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **mailboxId** | [**string**] | Filter by the mailbox resource ID the webhooks are attached to | (optional) defaults to undefined|
| **status** | [**&#39;active&#39; | &#39;disabled&#39; | &#39;paused&#39;**]**Array<&#39;active&#39; &#124; &#39;disabled&#39; &#124; &#39;paused&#39;>** | Filter webhooks by status | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListWebhooksV1200Response**

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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **regenerateWebhookSecretV1**
> MailV1WebhooksWebhookSecretResource regenerateWebhookSecretV1()

Regenerate the secret of a webhook. The previous secret is immediately invalidated. The new secret is returned only in this response and is sent as a bearer token with every delivery.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let webhookId: string; //Webhook ID (returned when the webhook was created) (default to undefined)

const { status, data } = await apiInstance.regenerateWebhookSecretV1(
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] | Webhook ID (returned when the webhook was created) | defaults to undefined|


### Return type

**MailV1WebhooksWebhookSecretResource**

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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **testWebhookV1**
> MailV1WebhooksWebhookTestResultResource testWebhookV1()

Send a test delivery to the webhook URL and return the result. Test requests are rate limited upstream.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let webhookId: string; //Webhook ID (returned when the webhook was created) (default to undefined)

const { status, data } = await apiInstance.testWebhookV1(
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] | Webhook ID (returned when the webhook was created) | defaults to undefined|


### Return type

**MailV1WebhooksWebhookTestResultResource**

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
|**422** | Error response |  -  |
|**429** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateWebhookV1**
> MailV1WebhooksWebhookResource updateWebhookV1(mailV1SchemaUpdateWebhookRequestSchema)

Partially update a webhook. Only the fields included in the request body are changed; omitted fields retain their current values. Pass `\"description\": null` to clear the description.

### Example

```typescript
import {
    MailWebhooksApi,
    Configuration,
    MailV1SchemaUpdateWebhookRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailWebhooksApi(configuration);

let webhookId: string; //Webhook ID (returned when the webhook was created) (default to undefined)
let mailV1SchemaUpdateWebhookRequestSchema: MailV1SchemaUpdateWebhookRequestSchema; //

const { status, data } = await apiInstance.updateWebhookV1(
    webhookId,
    mailV1SchemaUpdateWebhookRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaUpdateWebhookRequestSchema** | **MailV1SchemaUpdateWebhookRequestSchema**|  | |
| **webhookId** | [**string**] | Webhook ID (returned when the webhook was created) | defaults to undefined|


### Return type

**MailV1WebhooksWebhookResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**400** | Error response |  -  |
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

