# MailForwardersApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createForwarderV1**](#createforwarderv1) | **POST** /api/mail/v1/mailboxes/{mailboxId}/forwarders | Create forwarder|
|[**deleteForwarderV1**](#deleteforwarderv1) | **DELETE** /api/mail/v1/forwarders/{forwarderId} | Delete forwarder|
|[**listForwardersV1**](#listforwardersv1) | **GET** /api/mail/v1/orders/{orderId}/forwarders | List forwarders|
|[**resendForwarderConfirmationV1**](#resendforwarderconfirmationv1) | **POST** /api/mail/v1/forwarders/{forwarderId}/confirmation/resend | Resend forwarder confirmation|
|[**updateForwarderKeepCopySettingV1**](#updateforwarderkeepcopysettingv1) | **PATCH** /api/mail/v1/forwarders/{forwarderId}/keep-copy | Update forwarder keep-copy setting|

# **createForwarderV1**
> MailV1ForwardersForwarderResource createForwarderV1(mailV1SchemaCreateForwarderRequestSchema)

Create a forwarder from the given mailbox to the destination address. The destination receives a confirmation email and forwarding becomes active only after it is confirmed.

### Example

```typescript
import {
    MailForwardersApi,
    Configuration,
    MailV1SchemaCreateForwarderRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailForwardersApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)
let mailV1SchemaCreateForwarderRequestSchema: MailV1SchemaCreateForwarderRequestSchema; //

const { status, data } = await apiInstance.createForwarderV1(
    mailboxId,
    mailV1SchemaCreateForwarderRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaCreateForwarderRequestSchema** | **MailV1SchemaCreateForwarderRequestSchema**|  | |
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


### Return type

**MailV1ForwardersForwarderResource**

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

# **deleteForwarderV1**
> CommonSuccessEmptyResource deleteForwarderV1()

Delete a forwarder. The mailbox stops forwarding messages to the destination address immediately.

### Example

```typescript
import {
    MailForwardersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailForwardersApi(configuration);

let forwarderId: string; //Forwarder resource ID (default to undefined)

const { status, data } = await apiInstance.deleteForwarderV1(
    forwarderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **forwarderId** | [**string**] | Forwarder resource ID | defaults to undefined|


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

# **listForwardersV1**
> MailListForwardersV1200Response listForwardersV1()

Retrieve a paginated list of forwarders across all mailboxes of a mail order.

### Example

```typescript
import {
    MailForwardersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailForwardersApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listForwardersV1(
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

**MailListForwardersV1200Response**

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

# **resendForwarderConfirmationV1**
> CommonSuccessEmptyResource resendForwarderConfirmationV1()

Resend the confirmation email to the destination address of an unconfirmed forwarder.

### Example

```typescript
import {
    MailForwardersApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailForwardersApi(configuration);

let forwarderId: string; //Forwarder resource ID (default to undefined)

const { status, data } = await apiInstance.resendForwarderConfirmationV1(
    forwarderId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **forwarderId** | [**string**] | Forwarder resource ID | defaults to undefined|


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

# **updateForwarderKeepCopySettingV1**
> CommonSuccessEmptyResource updateForwarderKeepCopySettingV1(mailV1SchemaUpdateForwarderKeepCopyRequestSchema)

Enable or disable keeping a copy of forwarded messages in the mailbox.

### Example

```typescript
import {
    MailForwardersApi,
    Configuration,
    MailV1SchemaUpdateForwarderKeepCopyRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailForwardersApi(configuration);

let forwarderId: string; //Forwarder resource ID (default to undefined)
let mailV1SchemaUpdateForwarderKeepCopyRequestSchema: MailV1SchemaUpdateForwarderKeepCopyRequestSchema; //

const { status, data } = await apiInstance.updateForwarderKeepCopySettingV1(
    forwarderId,
    mailV1SchemaUpdateForwarderKeepCopyRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaUpdateForwarderKeepCopyRequestSchema** | **MailV1SchemaUpdateForwarderKeepCopyRequestSchema**|  | |
| **forwarderId** | [**string**] | Forwarder resource ID | defaults to undefined|


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
|**404** | Error response |  -  |
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

