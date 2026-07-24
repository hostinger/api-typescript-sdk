# MailAutorepliesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAutoreplyV1**](#createautoreplyv1) | **POST** /api/mail/v1/mailboxes/{mailboxId}/autoreplies | Create autoreply|
|[**deleteAutoreplyV1**](#deleteautoreplyv1) | **DELETE** /api/mail/v1/autoreplies/{autoreplyId} | Delete autoreply|
|[**listAutorepliesV1**](#listautorepliesv1) | **GET** /api/mail/v1/orders/{orderId}/autoreplies | List autoreplies|
|[**updateAutoreplyV1**](#updateautoreplyv1) | **PUT** /api/mail/v1/autoreplies/{autoreplyId} | Update autoreply|

# **createAutoreplyV1**
> MailV1AutorepliesAutoreplyResource createAutoreplyV1(mailV1SchemaUpsertAutoreplyRequestSchema)

Create an automatic reply for the given mailbox. A mailbox can have only one autoreply. Omit `starts_at` to activate the autoreply immediately and omit `ends_at` to keep it active indefinitely.

### Example

```typescript
import {
    MailAutorepliesApi,
    Configuration,
    MailV1SchemaUpsertAutoreplyRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAutorepliesApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)
let mailV1SchemaUpsertAutoreplyRequestSchema: MailV1SchemaUpsertAutoreplyRequestSchema; //

const { status, data } = await apiInstance.createAutoreplyV1(
    mailboxId,
    mailV1SchemaUpsertAutoreplyRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaUpsertAutoreplyRequestSchema** | **MailV1SchemaUpsertAutoreplyRequestSchema**|  | |
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


### Return type

**MailV1AutorepliesAutoreplyResource**

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
|**404** | Error response |  -  |
|**409** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAutoreplyV1**
> CommonSuccessEmptyResource deleteAutoreplyV1()

Delete the autoreply of a mailbox. The mailbox stops sending automatic replies immediately.

### Example

```typescript
import {
    MailAutorepliesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAutorepliesApi(configuration);

let autoreplyId: string; //Autoreply resource ID (default to undefined)

const { status, data } = await apiInstance.deleteAutoreplyV1(
    autoreplyId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **autoreplyId** | [**string**] | Autoreply resource ID | defaults to undefined|


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

# **listAutorepliesV1**
> MailListAutorepliesV1200Response listAutorepliesV1()

Retrieve a paginated list of autoreplies across all mailboxes of a mail order.

### Example

```typescript
import {
    MailAutorepliesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAutorepliesApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAutorepliesV1(
    orderId,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListAutorepliesV1200Response**

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

# **updateAutoreplyV1**
> MailV1AutorepliesAutoreplyResource updateAutoreplyV1(mailV1SchemaUpsertAutoreplyRequestSchema)

Replace the autoreply with the given content and schedule. Omitted optional fields are cleared: omit `starts_at` to activate the autoreply immediately and omit `ends_at` to keep it active indefinitely.

### Example

```typescript
import {
    MailAutorepliesApi,
    Configuration,
    MailV1SchemaUpsertAutoreplyRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAutorepliesApi(configuration);

let autoreplyId: string; //Autoreply resource ID (default to undefined)
let mailV1SchemaUpsertAutoreplyRequestSchema: MailV1SchemaUpsertAutoreplyRequestSchema; //

const { status, data } = await apiInstance.updateAutoreplyV1(
    autoreplyId,
    mailV1SchemaUpsertAutoreplyRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaUpsertAutoreplyRequestSchema** | **MailV1SchemaUpsertAutoreplyRequestSchema**|  | |
| **autoreplyId** | [**string**] | Autoreply resource ID | defaults to undefined|


### Return type

**MailV1AutorepliesAutoreplyResource**

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
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

