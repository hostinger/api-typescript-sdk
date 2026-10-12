# ReachProfilesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**connectSendingDomainV1**](#connectsendingdomainv1) | **POST** /api/reach/v1/profiles/{profileUuid}/domains | Connect sending domain|
|[**deleteSendingDomainV1**](#deletesendingdomainv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/domains | Delete sending domain|
|[**getConnectedSendingDomainV1**](#getconnectedsendingdomainv1) | **GET** /api/reach/v1/profiles/{profileUuid}/domains | Get connected sending domain|
|[**getProfileDomainDNSStatusV1**](#getprofiledomaindnsstatusv1) | **GET** /api/reach/v1/profiles/{profileUuid}/domains/dns-status | Get profile domain DNS status|
|[**getProfileSettingsV1**](#getprofilesettingsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/settings | Get profile settings|
|[**getRemainingPlanLimitsV1**](#getremainingplanlimitsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/limits | Get remaining plan limits|
|[**listPlanFeatureAccessV1**](#listplanfeatureaccessv1) | **GET** /api/reach/v1/profiles/{profileUuid}/features | List plan feature access|
|[**listProfilesV1**](#listprofilesv1) | **GET** /api/reach/v1/profiles | List Profiles|
|[**updateProfileSettingsV1**](#updateprofilesettingsv1) | **PATCH** /api/reach/v1/profiles/{profileUuid}/settings | Update profile settings|

# **connectSendingDomainV1**
> CommonSuccessEmptyResource connectSendingDomainV1(reachV1ProfilesDomainsConnectRequest)

Connect a sending domain to the profile so emails can be sent from addresses on it.  Connecting does not make the domain ready to send: check the DNS status endpoint next for records that are still missing. A domain the account owns or has already verified connects immediately. Any other domain starts a TXT ownership verification and returns `409`; complete the verification in Reach, then retry. Returns `422` when the profile or another profile already has the domain, the domain is blocked, or its ownership cannot be verified. An already connected domain is never replaced.  On success the sender address of draft and scheduled campaigns, and of published automation and double opt-in emails, moves onto the new domain in the background, keeping the part before the `@`.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration,
    ReachV1ProfilesDomainsConnectRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ProfilesDomainsConnectRequest: ReachV1ProfilesDomainsConnectRequest; //

const { status, data } = await apiInstance.connectSendingDomainV1(
    profileUuid,
    reachV1ProfilesDomainsConnectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ProfilesDomainsConnectRequest** | **ReachV1ProfilesDomainsConnectRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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
|**401** | Unauthenticated response |  -  |
|**409** | Conflict response. &#x60;Retry-After&#x60;, when present, is the number of seconds to wait before retrying. |  * Retry-After - Seconds to wait before retrying the request <br>  |
|**422** | Validation error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteSendingDomainV1**
> CommonSuccessEmptyResource deleteSendingDomainV1(reachV1ProfilesDomainsDisconnectRequest)

Disconnect the sending domain from the profile.  The domain record is removed, so the profile has no sending domain afterwards and campaigns cannot be sent until a domain is connected again. Sender addresses already stored on campaigns, automations and settings are left untouched and keep pointing at the removed domain. A domain that is not connected to the profile also succeeds, so success is not proof that anything was deleted. DNS records at the DNS provider are not removed. To switch domains, delete this one and connect the new one. Confirm the domain with the customer before calling.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration,
    ReachV1ProfilesDomainsDisconnectRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ProfilesDomainsDisconnectRequest: ReachV1ProfilesDomainsDisconnectRequest; //

const { status, data } = await apiInstance.deleteSendingDomainV1(
    profileUuid,
    reachV1ProfilesDomainsDisconnectRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ProfilesDomainsDisconnectRequest** | **ReachV1ProfilesDomainsDisconnectRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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

# **getProfileSettingsV1**
> ReachV1ProfilesSettingsSettingsResource getProfileSettingsV1()

Get the profile\'s saved sender identity and brand details.  Read the default sender before creating a campaign instead of asking the customer, and reuse the brand fields when generating email content. Any field can be `null` for a profile that never filled its settings in. This does not check that the sending domain is verified, use the connected sending domain endpoint for that.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.getProfileSettingsV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ProfilesSettingsSettingsResource**

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

# **updateProfileSettingsV1**
> ReachV1ProfilesSettingsSettingsResource updateProfileSettingsV1(reachV1ProfilesSettingsUpdateRequest)

Change the profile\'s default sender and brand details.  Send only the fields to change: every omitted field keeps its value, and `null` or an empty string clears a text field. The default sender is what campaigns created afterwards start from; existing campaigns keep their own sender. `sender_email` is only the part before the `@`, because Reach combines it with the profile\'s connected sending domain, so an address outside that domain cannot be set. Connecting a sending domain is a separate endpoint and a connected domain cannot be changed here. Returns the settings after the change.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration,
    ReachV1ProfilesSettingsUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ProfilesSettingsUpdateRequest: ReachV1ProfilesSettingsUpdateRequest; //

const { status, data } = await apiInstance.updateProfileSettingsV1(
    profileUuid,
    reachV1ProfilesSettingsUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ProfilesSettingsUpdateRequest** | **ReachV1ProfilesSettingsUpdateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ProfilesSettingsSettingsResource**

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

