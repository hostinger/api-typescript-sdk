# MailCatchallsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createCatchAllV1**](#createcatchallv1) | **POST** /api/mail/v1/mailboxes/{mailboxId}/catchalls | Create catch-all|
|[**deleteCatchAllV1**](#deletecatchallv1) | **DELETE** /api/mail/v1/catchalls/{catchallId} | Delete catch-all|
|[**listCatchAllsV1**](#listcatchallsv1) | **GET** /api/mail/v1/orders/{orderId}/catchalls | List catch-alls|
|[**resendCatchAllConfirmationV1**](#resendcatchallconfirmationv1) | **POST** /api/mail/v1/catchalls/{catchallId}/confirmation/resend | Resend catch-all confirmation|

# **createCatchAllV1**
> MailV1CatchallsCatchallResource createCatchAllV1()

Create a catch-all that routes all messages sent to unknown addresses of the domain to the given mailbox. The mailbox address receives a confirmation email and the catch-all becomes active only after it is confirmed. A domain can have only one catch-all.

### Example

```typescript
import {
    MailCatchallsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailCatchallsApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)

const { status, data } = await apiInstance.createCatchAllV1(
    mailboxId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


### Return type

**MailV1CatchallsCatchallResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
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

# **deleteCatchAllV1**
> CommonSuccessEmptyResource deleteCatchAllV1()

Delete a catch-all. Messages sent to unknown addresses of the domain are no longer routed to the mailbox.

### Example

```typescript
import {
    MailCatchallsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailCatchallsApi(configuration);

let catchallId: string; //Catch-all resource ID (default to undefined)

const { status, data } = await apiInstance.deleteCatchAllV1(
    catchallId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **catchallId** | [**string**] | Catch-all resource ID | defaults to undefined|


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

# **listCatchAllsV1**
> MailListCatchAllsV1200Response listCatchAllsV1()

Retrieve a paginated list of catch-alls across all mailboxes of a mail order.

### Example

```typescript
import {
    MailCatchallsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailCatchallsApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listCatchAllsV1(
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

**MailListCatchAllsV1200Response**

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

# **resendCatchAllConfirmationV1**
> CommonSuccessEmptyResource resendCatchAllConfirmationV1()

Resend the confirmation email to the mailbox address of an unconfirmed catch-all.

### Example

```typescript
import {
    MailCatchallsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailCatchallsApi(configuration);

let catchallId: string; //Catch-all resource ID (default to undefined)

const { status, data } = await apiInstance.resendCatchAllConfirmationV1(
    catchallId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **catchallId** | [**string**] | Catch-all resource ID | defaults to undefined|


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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

