# DomainsTransferApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**claimFreeDomainTransferV1**](#claimfreedomaintransferv1) | **POST** /api/domains/v1/transfers/claim | Claim free domain transfer|
|[**getTransferListV1**](#gettransferlistv1) | **GET** /api/domains/v1/transfers | Get transfer list|
|[**getTransferV1**](#gettransferv1) | **GET** /api/domains/v1/transfers/{domain} | Get transfer|

# **claimFreeDomainTransferV1**
> DomainsV1TransferTransferResource claimFreeDomainTransferV1(domainsV1TransferClaimRequest)

Claim a free domain transfer available on your account and start the transfer.  Unlike purchasing a transfer, this consumes a free domain transfer you already have, so no payment method is required.  Before making request, unlock the domain at the current registrar and get its authorization code. The transfer is validated first, so domains which cannot be transferred are rejected before the free domain transfer is consumed.  A successful response means the transfer has been started. Completion depends on the current registrar and can be followed with the [transfer list endpoint](#tag/domains-transfer).  If no WHOIS information is provided, default contact information for that TLD will be used. Before making request, ensure WHOIS information for desired TLD exists in your account.  Requests which cannot be fulfilled are rejected with an error code in the response body.  Use this endpoint to transfer a domain using a free domain transfer from your account.

### Example

```typescript
import {
    DomainsTransferApi,
    Configuration,
    DomainsV1TransferClaimRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsTransferApi(configuration);

let domainsV1TransferClaimRequest: DomainsV1TransferClaimRequest; //

const { status, data } = await apiInstance.claimFreeDomainTransferV1(
    domainsV1TransferClaimRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1TransferClaimRequest** | **DomainsV1TransferClaimRequest**|  | |


### Return type

**DomainsV1TransferTransferResource**

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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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

