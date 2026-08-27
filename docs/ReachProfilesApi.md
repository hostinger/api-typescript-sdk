# ReachProfilesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getConnectedSendingDomainV1**](#getconnectedsendingdomainv1) | **GET** /api/reach/v1/profiles/{profileUuid}/domains | Get connected sending domain|
|[**getProfileDomainDNSStatusV1**](#getprofiledomaindnsstatusv1) | **GET** /api/reach/v1/profiles/{profileUuid}/domains/dns-status | Get profile domain DNS status|
|[**getRemainingPlanLimitsV1**](#getremainingplanlimitsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/limits | Get remaining plan limits|
|[**listPlanFeatureAccessV1**](#listplanfeatureaccessv1) | **GET** /api/reach/v1/profiles/{profileUuid}/features | List plan feature access|
|[**listProfilesV1**](#listprofilesv1) | **GET** /api/reach/v1/profiles | List Profiles|

# **getConnectedSendingDomainV1**
> ReachV1ProfilesDomainsSendingDomainResource getConnectedSendingDomainV1()

Get the sending domain connected to the profile, its verification status and any suspended sender addresses.  Campaigns only go out once a domain is connected and active, so this is the cheapest way to check that precondition before building one. A profile with no domain connected returns the same shape with every field set to `null`. For the individual MX, SPF, DKIM and DMARC records behind the status, use the DNS status endpoint.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.getConnectedSendingDomainV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ProfilesDomainsSendingDomainResource**

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

# **getProfileDomainDNSStatusV1**
> ReachV1ProfilesDomainsDnsStatusResource getProfileDomainDNSStatusV1()

Retrieve the DNS configuration status for a profile\'s domain.  This endpoint reports the state of MX, SPF, DKIM and DMARC records, including the actual records found and the suggested records required for correct email delivery.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.getProfileDomainDNSStatusV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ProfilesDomainsDnsStatusResource**

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

# **getRemainingPlanLimitsV1**
> ReachV1ProfilesPlanLimitsResource getRemainingPlanLimitsV1()

Get how much of the plan is left for the current period.  Two things to keep in mind before you build alerting on this. The period is a calendar month rather than a billing anniversary, so the counters reset on the 1st no matter when the subscription started. And usage is tracked per order, so every profile on the same order shares one pool and reports the same numbers here. Only the current period is available, past usage is not kept.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.getRemainingPlanLimitsV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ProfilesPlanLimitsResource**

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

# **listPlanFeatureAccessV1**
> Array<ReachV1ProfilesFeaturesPlanFeatureResource> listPlanFeatureAccessV1()

List which plan features the profile can use.  This is the feature lock matrix, not a usage quota. `available` means the feature can be used right now and `locked` means it is not part of the base plan, so an upgrade is needed. For remaining emails, recipients and AI credits use the limits endpoint instead.  Worth checking before building something that cannot be activated afterwards, such as an automation on a plan without automation activation.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listPlanFeatureAccessV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1ProfilesFeaturesPlanFeatureResource>**

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

# **listProfilesV1**
> Array<ReachV1ProfilesProfileResource> listProfilesV1()

This endpoint returns all profiles available to the client, including their basic information.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

const { status, data } = await apiInstance.listProfilesV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<ReachV1ProfilesProfileResource>**

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

