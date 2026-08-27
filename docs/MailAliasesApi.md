# MailAliasesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAliasV1**](#createaliasv1) | **POST** /api/mail/v1/mailboxes/{mailboxId}/aliases | Create alias|
|[**deleteAliasV1**](#deletealiasv1) | **DELETE** /api/mail/v1/aliases/{aliasId} | Delete alias|
|[**listAliasesV1**](#listaliasesv1) | **GET** /api/mail/v1/orders/{orderId}/aliases | List aliases|

# **createAliasV1**
> MailV1AliasesAliasResource createAliasV1(mailV1SchemaCreateAliasRequestSchema)

Create an alias for the given mailbox. The alias address is formed from the given local part and the domain of the mailbox. Messages sent to the alias are delivered to the mailbox.

### Example

```typescript
import {
    MailAliasesApi,
    Configuration,
    MailV1SchemaCreateAliasRequestSchema
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailAliasesApi(configuration);

let mailboxId: string; //Mailbox resource ID (default to undefined)
let mailV1SchemaCreateAliasRequestSchema: MailV1SchemaCreateAliasRequestSchema; //

const { status, data } = await apiInstance.createAliasV1(
    mailboxId,
    mailV1SchemaCreateAliasRequestSchema
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **mailV1SchemaCreateAliasRequestSchema** | **MailV1SchemaCreateAliasRequestSchema**|  | |
| **mailboxId** | [**string**] | Mailbox resource ID | defaults to undefined|


### Return type

**MailV1AliasesAliasResource**

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

# **deleteAliasV1**
> CommonSuccessEmptyResource deleteAliasV1()

Delete an alias. Messages sent to the alias address are no longer delivered to the mailbox.

### Example

```typescript
import {
    MailAliasesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailAliasesApi(configuration);

let aliasId: string; //Alias resource ID (default to undefined)

const { status, data } = await apiInstance.deleteAliasV1(
    aliasId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **aliasId** | [**string**] | Alias resource ID | defaults to undefined|


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

# **listAliasesV1**
> MailListAliasesV1200Response listAliasesV1()

Retrieve a paginated list of aliases across all mailboxes of a mail order.

### Example

```typescript
import {
    MailAliasesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new MailAliasesApi(configuration);

let orderId: string; //Order resource ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAliasesV1(
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

**MailListAliasesV1200Response**

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

