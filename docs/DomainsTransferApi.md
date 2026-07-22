# DomainsTransferApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getTransferListV1**](#gettransferlistv1) | **GET** /api/domains/v1/transfers | Get transfer list|
|[**getTransferV1**](#gettransferv1) | **GET** /api/domains/v1/transfers/{domain} | Get transfer|

# **getTransferListV1**
> Array<DomainsV1TransferTransferResource> getTransferListV1()

Retrieve all domain transfers in your portfolio.  Use this endpoint to monitor incoming and outgoing registrar transfers across your domains.

### Example

```typescript
import {
    DomainsTransferApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsTransferApi(configuration);

const { status, data } = await apiInstance.getTransferListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<DomainsV1TransferTransferResource>**

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

# **getTransferV1**
> DomainsV1TransferTransferResource getTransferV1()

Retrieve the transfer for a specified domain.  Use this endpoint to track an incoming or outgoing registrar transfer and its status.

### Example

```typescript
import {
    DomainsTransferApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsTransferApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getTransferV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1TransferTransferResource**

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

