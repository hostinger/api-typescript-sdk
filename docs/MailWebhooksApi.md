# MailWebhooksApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebhookV1**](#createwebhookv1) | **POST** /api/mail/v1/mailboxes/{mailboxId}/webhooks | Create webhook|

# **createWebhookV1**
> MailV1WebhooksWebhookResource createWebhookV1(mailV1SchemaCreateWebhookRequestSchema)

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

**MailV1WebhooksWebhookResource**

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

