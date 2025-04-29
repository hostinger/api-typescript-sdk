# DomainsForwardingApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createForwardingDataV1**](#createforwardingdatav1) | **POST** /api/domains/v1/forwarding | Create forwarding data|
|[**deleteForwardingDataV1**](#deleteforwardingdatav1) | **DELETE** /api/domains/v1/forwarding/{domain} | Delete forwarding data|
|[**getForwardingDataV1**](#getforwardingdatav1) | **GET** /api/domains/v1/forwarding/{domain} | Get forwarding data|

# **createForwardingDataV1**
> DomainsV1ForwardingForwardingResource createForwardingDataV1(domainsV1ForwardingStoreRequest)

This endpoint creates domain forwarding data.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration,
    DomainsV1ForwardingStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domainsV1ForwardingStoreRequest: DomainsV1ForwardingStoreRequest; //

const { status, data } = await apiInstance.createForwardingDataV1(
    domainsV1ForwardingStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1ForwardingStoreRequest** | **DomainsV1ForwardingStoreRequest**|  | |


### Return type

**DomainsV1ForwardingForwardingResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteForwardingDataV1**
> CommonSuccessEmptyResource deleteForwardingDataV1()

This endpoint deletes domain forwarding data.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.deleteForwardingDataV1(
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
|**200** | Success response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getForwardingDataV1**
> DomainsV1ForwardingForwardingResource getForwardingDataV1()

This endpoint retrieves domain forwarding data.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getForwardingDataV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1ForwardingForwardingResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

