# MailAPITokensApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAPITokenV1**](#createapitokenv1) | **POST** /api/mail/v1/orders/{orderId}/api-tokens | Create API token|
|[**listAPITokensV1**](#listapitokensv1) | **GET** /api/mail/v1/api-tokens | List API tokens|
|[**revokeAPITokenV1**](#revokeapitokenv1) | **DELETE** /api/mail/v1/api-tokens/{tokenId} | Revoke API token|

# **createAPITokenV1**
> MailV1ApiTokensApiTokenCreatedResource createAPITokenV1(mailV1SchemaCreateApiTokenRequestSchema)

Create an API token for the given mail order. The token grants access to the [Hostinger Email API](https://api.mail.hostinger.com/), where you can provision and manage the mailboxes it is scoped to.  The plaintext token is returned only in this response, never again. A maximum of 10 tokens can exist per order. Use `scope.has_all_mailboxes` to cover all current and future mailboxes, or list specific mailboxes in `scope.mailbox_ids`.

### Example

```typescript
import {
    MailAPITokensApi,
    Configuration,
    MailV1SchemaCreateApiTokenRequestSchema
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAPITokensApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let mailV1SchemaCreateApiTokenRequestSchema: MailV1SchemaCreateApiTokenRequestSchema; //

const { status, data } = await apiInstance.createAPITokenV1(
    orderId,
    mailV1SchemaCreateApiTokenRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaCreateApiTokenRequestSchema** | **MailV1SchemaCreateApiTokenRequestSchema**|  | |
| **orderId** | [**string**] | Order resource ID | defaults to undefined|


### Return type

**MailV1ApiTokensApiTokenCreatedResource**

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

# **listAPITokensV1**
> MailListAPITokensV1200Response listAPITokensV1()

Retrieve a paginated list of [Hostinger Email API](https://api.mail.hostinger.com/) tokens across all your mail orders, optionally filtered by order. Plaintext tokens are never included; they are returned only when a token is created.

### Example

```typescript
import {
    MailAPITokensApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAPITokensApi(configuration);

let orderId: string; //Filter tokens by order resource ID. Single value or comma-separated list. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAPITokensV1(
    orderId,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**string**] | Filter tokens by order resource ID. Single value or comma-separated list. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**MailListAPITokensV1200Response**

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
|**422** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revokeAPITokenV1**
> CommonSuccessEmptyResource revokeAPITokenV1()

Revoke an API token. The token immediately loses access to the [Hostinger Email API](https://api.mail.hostinger.com/). This action cannot be undone.

### Example

```typescript
import {
    MailAPITokensApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new MailAPITokensApi(configuration);

let tokenId: string; //API token ID (returned when the token was created) (default to undefined)

const { status, data } = await apiInstance.revokeAPITokenV1(
    tokenId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tokenId** | [**string**] | API token ID (returned when the token was created) | defaults to undefined|


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

