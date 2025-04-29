# DomainsAvailabilityApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**checkDomainAvailabilityV1**](#checkdomainavailabilityv1) | **POST** /api/domains/v1/availability | Check domain availability|

# **checkDomainAvailabilityV1**
> Array<DomainsV1AvailabilityAvailabilityResource> checkDomainAvailabilityV1(domainsV1AvailabilityAvailabilityRequest)

This endpoint checks the availability of a domain name. Multiple TLDs can be checked at once.  Endpoint has rate limit of 10 requests per minute.

### Example

```typescript
import {
    DomainsAvailabilityApi,
    Configuration,
    DomainsV1AvailabilityAvailabilityRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsAvailabilityApi(configuration);

let domainsV1AvailabilityAvailabilityRequest: DomainsV1AvailabilityAvailabilityRequest; //

const { status, data } = await apiInstance.checkDomainAvailabilityV1(
    domainsV1AvailabilityAvailabilityRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1AvailabilityAvailabilityRequest** | **DomainsV1AvailabilityAvailabilityRequest**|  | |


### Return type

**Array<DomainsV1AvailabilityAvailabilityResource>**

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

