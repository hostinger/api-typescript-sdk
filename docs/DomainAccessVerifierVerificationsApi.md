# DomainAccessVerifierVerificationsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getDomainVerificationsDIRECT**](#getdomainverificationsdirect) | **GET** /api/v2/direct/verifications/active | Get domain verifications|

# **getDomainVerificationsDIRECT**
> DomainAccessVerifierV2VerificationsActiveVerificationsCollection getDomainVerificationsDIRECT(domainAccessVerifierV2VerificationsListRequest)

Retrieve a list of pending and completed domain verifications.

### Example

```typescript
import {
    DomainAccessVerifierVerificationsApi,
    Configuration,
    DomainAccessVerifierV2VerificationsListRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainAccessVerifierVerificationsApi(configuration);

let domainAccessVerifierV2VerificationsListRequest: DomainAccessVerifierV2VerificationsListRequest; //

const { status, data } = await apiInstance.getDomainVerificationsDIRECT(
    domainAccessVerifierV2VerificationsListRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainAccessVerifierV2VerificationsListRequest** | **DomainAccessVerifierV2VerificationsListRequest**|  | |


### Return type

**DomainAccessVerifierV2VerificationsActiveVerificationsCollection**

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
|**422** | Validation error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

