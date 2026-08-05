# DomainsMoveApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**acceptIncomingDomainMoveV1**](#acceptincomingdomainmovev1) | **PUT** /api/domains/v1/move/incoming/{domain} | Accept incoming domain move|
|[**cancelOutgoingDomainMoveV1**](#canceloutgoingdomainmovev1) | **DELETE** /api/domains/v1/move/outgoing/{domain} | Cancel outgoing domain move|
|[**getIncomingDomainMoveListV1**](#getincomingdomainmovelistv1) | **GET** /api/domains/v1/move/incoming | Get incoming domain move list|
|[**getIncomingDomainMoveV1**](#getincomingdomainmovev1) | **GET** /api/domains/v1/move/incoming/{domain} | Get incoming domain move|
|[**getOutgoingDomainMoveListV1**](#getoutgoingdomainmovelistv1) | **GET** /api/domains/v1/move/outgoing | Get outgoing domain move list|
|[**getOutgoingDomainMoveV1**](#getoutgoingdomainmovev1) | **GET** /api/domains/v1/move/outgoing/{domain} | Get outgoing domain move|
|[**rejectIncomingDomainMoveV1**](#rejectincomingdomainmovev1) | **DELETE** /api/domains/v1/move/incoming/{domain} | Reject incoming domain move|
|[**startOutgoingDomainMoveV1**](#startoutgoingdomainmovev1) | **POST** /api/domains/v1/move/outgoing/{domain} | Start outgoing domain move|

# **acceptIncomingDomainMoveV1**
> CommonSuccessEmptyResource acceptIncomingDomainMoveV1(domainsV1MoveIncomingUpdateRequest)

Accept an incoming move for a specified domain.  The provided WHOIS profiles become the contacts of the domain, so they must belong to your account and satisfy the requirements of the TLD. Only the contact types the domain actually uses are applied, but all four profile IDs have to be provided.  The move has to still be waiting for your decision, already accepted moves cannot be accepted again.  Accepting does not complete the move. A confirmation email is sent to the email address of the new owner contact, and the domain changes hands only after the change is confirmed from it. Until then the move stays in the `activating` status, which can be followed with the [incoming move endpoint](#tag/domains-move).  Use this endpoint to take ownership of a domain offered to you.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration,
    DomainsV1MoveIncomingUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

let domain: string; //Domain name (default to undefined)
let domainsV1MoveIncomingUpdateRequest: DomainsV1MoveIncomingUpdateRequest; //

const { status, data } = await apiInstance.acceptIncomingDomainMoveV1(
    domain,
    domainsV1MoveIncomingUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1MoveIncomingUpdateRequest** | **DomainsV1MoveIncomingUpdateRequest**|  | |
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **cancelOutgoingDomainMoveV1**
> CommonSuccessEmptyResource cancelOutgoingDomainMoveV1()

Cancel an outgoing move for a specified domain.  The move can only be cancelled while the receiving account has not accepted it yet. The domain stays in your account.  Use this endpoint to withdraw a move you no longer want to complete.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.cancelOutgoingDomainMoveV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**200** | Success empty response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getIncomingDomainMoveListV1**
> Array<DomainsV1MoveMoveResource> getIncomingDomainMoveListV1()

Retrieve all domains other Hostinger accounts are moving to your account.  Moves of every status are returned, including the ones which already completed.  Use this endpoint to find domains waiting for you to accept them.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

const { status, data } = await apiInstance.getIncomingDomainMoveListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<DomainsV1MoveMoveResource>**

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

# **getIncomingDomainMoveV1**
> DomainsV1MoveMoveResource getIncomingDomainMoveV1()

Retrieve the incoming move for a specified domain.  Returns 404 when no account is moving this domain to you.  Use this endpoint to check whether a domain addressed to you is still waiting to be accepted.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

let domain: string; //Domain name (default to undefined)
let forceSync: boolean; //Re-check the move against the registry before responding. Only has an effect while the move is in the `activating` status. (optional) (default to false)

const { status, data } = await apiInstance.getIncomingDomainMoveV1(
    domain,
    forceSync
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **forceSync** | [**boolean**] | Re-check the move against the registry before responding. Only has an effect while the move is in the &#x60;activating&#x60; status. | (optional) defaults to false|


### Return type

**DomainsV1MoveMoveResource**

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

# **getOutgoingDomainMoveListV1**
> Array<DomainsV1MoveMoveResource> getOutgoingDomainMoveListV1()

Retrieve all domains you are moving to other Hostinger accounts.  Only moves which have not completed yet are returned.  Use this endpoint to track moves you have initiated and the accounts they are addressed to.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

const { status, data } = await apiInstance.getOutgoingDomainMoveListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<DomainsV1MoveMoveResource>**

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

# **getOutgoingDomainMoveV1**
> DomainsV1MoveMoveResource getOutgoingDomainMoveV1()

Retrieve the outgoing move for a specified domain.  Returns 404 when the domain has no move in progress.  Use this endpoint to track the status of a move you have initiated for a single domain.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getOutgoingDomainMoveV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1MoveMoveResource**

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

# **rejectIncomingDomainMoveV1**
> CommonSuccessEmptyResource rejectIncomingDomainMoveV1()

Reject an incoming move for a specified domain.  The domain stays in the account which initiated the move. Moves you have already accepted cannot be rejected anymore.  Use this endpoint to decline a domain you do not want to take over.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.rejectIncomingDomainMoveV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**200** | Success empty response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **startOutgoingDomainMoveV1**
> CommonSuccessEmptyResource startOutgoingDomainMoveV1(domainsV1MoveOutgoingStoreRequest)

Initiate a move of a specified domain to another Hostinger account.  The receiving account has to already exist and accept the move before the domain changes hands.  The domain must be active. The subscription it belongs to is resolved automatically, and the request is rejected with a 404 status code when the domain has no domain subscription of its own.  Domains protected by premium protection require an additional verification step, such requests are rejected with a 428 status code.  Use this endpoint to hand a domain over to another Hostinger user.

### Example

```typescript
import {
    DomainsMoveApi,
    Configuration,
    DomainsV1MoveOutgoingStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsMoveApi(configuration);

let domain: string; //Domain name (default to undefined)
let domainsV1MoveOutgoingStoreRequest: DomainsV1MoveOutgoingStoreRequest; //

const { status, data } = await apiInstance.startOutgoingDomainMoveV1(
    domain,
    domainsV1MoveOutgoingStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1MoveOutgoingStoreRequest** | **DomainsV1MoveOutgoingStoreRequest**|  | |
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

