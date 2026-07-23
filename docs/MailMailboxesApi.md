# MailMailboxesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**changeMailboxPasswordV1**](#changemailboxpasswordv1) | **PATCH** /api/mail/v1/mailboxes/{mailboxId}/password | Change mailbox password|
|[**createMailboxV1**](#createmailboxv1) | **POST** /api/mail/v1/orders/{orderId}/mailboxes | Create mailbox|
|[**deleteMailboxV1**](#deletemailboxv1) | **DELETE** /api/mail/v1/mailboxes/{mailboxId} | Delete mailbox|
|[**listMailboxesV1**](#listmailboxesv1) | **GET** /api/mail/v1/orders/{orderId}/mailboxes | List mailboxes|

# **changeMailboxPasswordV1**
> CommonSuccessEmptyResource changeMailboxPasswordV1(mailV1SchemaChangeMailboxPasswordRequestSchema)

Change the password of a mailbox.

### Example

```typescript
import {
    MailMailboxesApi,
    Configuration,
    MailV1SchemaChangeMailboxPasswordRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailMailboxesApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)
let mailV1SchemaChangeMailboxPasswordRequestSchema: MailV1SchemaChangeMailboxPasswordRequestSchema; //

const { status, data } = await apiInstance.changeMailboxPasswordV1(
    mailboxId,
    mailV1SchemaChangeMailboxPasswordRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaChangeMailboxPasswordRequestSchema** | **MailV1SchemaChangeMailboxPasswordRequestSchema**|  | |
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

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

# **createMailboxV1**
> MailV1MailboxesMailboxResource createMailboxV1(mailV1SchemaCreateMailboxRequestSchema)

Create a mailbox under the given mail order. The full email address is composed from the given local part and the domain of the order.

### Example

```typescript
import {
    MailMailboxesApi,
    Configuration,
    MailV1SchemaCreateMailboxRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailMailboxesApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let mailV1SchemaCreateMailboxRequestSchema: MailV1SchemaCreateMailboxRequestSchema; //

const { status, data } = await apiInstance.createMailboxV1(
    orderId,
    mailV1SchemaCreateMailboxRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaCreateMailboxRequestSchema** | **MailV1SchemaCreateMailboxRequestSchema**|  | |
| **orderId** | [**string**] | Order resource ID | defaults to undefined|


### Return type

**MailV1MailboxesMailboxResource**

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

# **deleteMailboxV1**
> CommonSuccessEmptyResource deleteMailboxV1()

Delete a mailbox. The mailbox is soft-deleted and stays restorable for a limited period before it is permanently removed.

### Example

```typescript
import {
    MailMailboxesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailMailboxesApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)

const { status, data } = await apiInstance.deleteMailboxV1(
    mailboxId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


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
|**409** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listMailboxesV1**
> MailListMailboxesV1200Response listMailboxesV1()

Retrieve a paginated list of mailboxes belonging to a mail order.  Use this endpoint to monitor mailboxes of your mail service, including their status, enabled protocols, attached resource counts, and periodically synced usage numbers (usage may lag behind live values).

### Example

```typescript
import {
    MailMailboxesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailMailboxesApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let search: string; //Filter mailboxes whose email address contains the given string (optional) (default to undefined)
let sort: 'address' | '-address'; //Sort mailboxes by field. Prefix with `-` for descending order. (optional) (default to 'address')
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listMailboxesV1(
    orderId,
    search,
    sort,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Order resource ID | defaults to undefined|
| **search** | [**string**] | Filter mailboxes whose email address contains the given string | (optional) defaults to undefined|
| **sort** | [**&#39;address&#39; | &#39;-address&#39;**]**Array<&#39;address&#39; &#124; &#39;-address&#39;>** | Sort mailboxes by field. Prefix with &#x60;-&#x60; for descending order. | (optional) defaults to 'address'|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListMailboxesV1200Response**

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

