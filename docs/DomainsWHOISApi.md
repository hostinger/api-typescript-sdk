# DomainsWHOISApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**cancelPendingIRTPVerificationV1**](#cancelpendingirtpverificationv1) | **DELETE** /api/domains/v1/irtp/{domain} | Cancel pending IRTP verification|
|[**changeWHOISProfileForDomainV1**](#changewhoisprofilefordomainv1) | **PUT** /api/domains/v1/whois/change | Change WHOIS profile for domain|
|[**createWHOISProfileV1**](#createwhoisprofilev1) | **POST** /api/domains/v1/whois | Create WHOIS profile|
|[**deleteWHOISProfileV1**](#deletewhoisprofilev1) | **DELETE** /api/domains/v1/whois/{whoisId} | Delete WHOIS profile|
|[**getPendingIRTPVerificationV1**](#getpendingirtpverificationv1) | **GET** /api/domains/v1/irtp/{domain} | Get pending IRTP verification|
|[**getWHOISProfileListV1**](#getwhoisprofilelistv1) | **GET** /api/domains/v1/whois | Get WHOIS profile list|
|[**getWHOISProfileUsageV1**](#getwhoisprofileusagev1) | **GET** /api/domains/v1/whois/{whoisId}/usage | Get WHOIS profile usage|
|[**getWHOISProfileV1**](#getwhoisprofilev1) | **GET** /api/domains/v1/whois/{whoisId} | Get WHOIS profile|
|[**setWHOISProfileAsDefaultV1**](#setwhoisprofileasdefaultv1) | **PUT** /api/domains/v1/whois/default/{whoisId} | Set WHOIS profile as default|
|[**unsetDefaultWHOISProfileV1**](#unsetdefaultwhoisprofilev1) | **DELETE** /api/domains/v1/whois/default/{whoisId} | Unset default WHOIS profile|

# **cancelPendingIRTPVerificationV1**
> CommonSuccessEmptyResource cancelPendingIRTPVerificationV1()

Cancel a pending IRTP verification.  Use this endpoint to back out of a WHOIS change that is stuck waiting on registrant confirmation, for example when the confirmation email cannot be received, without waiting out the 5-day expiry.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.cancelPendingIRTPVerificationV1(
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

# **changeWHOISProfileForDomainV1**
> CommonSuccessEmptyResource changeWHOISProfileForDomainV1(domainsV1WHOISChangeUpdateRequest)

Change WHOIS contact profile for a domain.  Repoints the given contact roles to a new WHOIS profile and submits the change to the registry. The profile currently assigned to those roles is resolved automatically; the request fails if the given roles are not all on the same profile today.  Changing transfer sensitive fields on the owner contact starts an IRTP verification.  The change is processed asynchronously.  Use this endpoint to move a registered domain onto different contact information.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration,
    DomainsV1WHOISChangeUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let domainsV1WHOISChangeUpdateRequest: DomainsV1WHOISChangeUpdateRequest; //

const { status, data } = await apiInstance.changeWHOISProfileForDomainV1(
    domainsV1WHOISChangeUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1WHOISChangeUpdateRequest** | **DomainsV1WHOISChangeUpdateRequest**|  | |


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

# **createWHOISProfileV1**
> DomainsV1WHOISProfileResource createWHOISProfileV1(domainsV1WHOISStoreRequest)

Create WHOIS contact profile.  Use this endpoint to add new contact information for domain registration.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration,
    DomainsV1WHOISStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let domainsV1WHOISStoreRequest: DomainsV1WHOISStoreRequest; //

const { status, data } = await apiInstance.createWHOISProfileV1(
    domainsV1WHOISStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1WHOISStoreRequest** | **DomainsV1WHOISStoreRequest**|  | |


### Return type

**DomainsV1WHOISProfileResource**

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

# **deleteWHOISProfileV1**
> CommonSuccessEmptyResource deleteWHOISProfileV1()

Delete WHOIS contact profile.  Use this endpoint to remove unused contact profiles from account.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let whoisId: number; //WHOIS ID (default to undefined)

const { status, data } = await apiInstance.deleteWHOISProfileV1(
    whoisId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **whoisId** | [**number**] | WHOIS ID | defaults to undefined|


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
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPendingIRTPVerificationV1**
> DomainsV1IRTPVerificationResource getPendingIRTPVerificationV1()

Retrieve a pending IRTP verification for a domain.  Both the old and new registrant must confirm it before the WHOIS change takes effect.  Use this endpoint to check the status of a WHOIS change awaiting registrant confirmation.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getPendingIRTPVerificationV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1IRTPVerificationResource**

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

# **getWHOISProfileListV1**
> Array<DomainsV1WHOISProfileResource> getWHOISProfileListV1()

Retrieve WHOIS contact profiles.  Use this endpoint to view available contact profiles for domain registration.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let tld: string; //Filter by TLD (without leading dot) (optional) (default to undefined)

const { status, data } = await apiInstance.getWHOISProfileListV1(
    tld
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tld** | [**string**] | Filter by TLD (without leading dot) | (optional) defaults to undefined|


### Return type

**Array<DomainsV1WHOISProfileResource>**

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

# **getWHOISProfileUsageV1**
> Array<string> getWHOISProfileUsageV1()

Retrieve domain list where provided WHOIS contact profile is used.  Use this endpoint to view which domains use specific contact profiles.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let whoisId: number; //WHOIS ID (default to undefined)

const { status, data } = await apiInstance.getWHOISProfileUsageV1(
    whoisId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **whoisId** | [**number**] | WHOIS ID | defaults to undefined|


### Return type

**Array<string>**

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

# **getWHOISProfileV1**
> DomainsV1WHOISProfileResource getWHOISProfileV1()

Retrieve a WHOIS contact profile.  Use this endpoint to view domain registration contact information.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let whoisId: number; //WHOIS ID (default to undefined)

const { status, data } = await apiInstance.getWHOISProfileV1(
    whoisId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **whoisId** | [**number**] | WHOIS ID | defaults to undefined|


### Return type

**DomainsV1WHOISProfileResource**

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

# **setWHOISProfileAsDefaultV1**
> CommonSuccessEmptyResource setWHOISProfileAsDefaultV1()

Set WHOIS contact profile as default.  The default profile is pre-selected for the TLD it belongs to when registering new domains.  Use this endpoint to avoid picking contact information for every registration.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let whoisId: number; //WHOIS ID (default to undefined)

const { status, data } = await apiInstance.setWHOISProfileAsDefaultV1(
    whoisId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **whoisId** | [**number**] | WHOIS ID | defaults to undefined|


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

# **unsetDefaultWHOISProfileV1**
> CommonSuccessEmptyResource unsetDefaultWHOISProfileV1()

Unset WHOIS contact profile as default.  The profile itself is kept, it is only no longer pre-selected for its TLD.  Use this endpoint to stop reusing contact information for new registrations.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let whoisId: number; //WHOIS ID (default to undefined)

const { status, data } = await apiInstance.unsetDefaultWHOISProfileV1(
    whoisId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **whoisId** | [**number**] | WHOIS ID | defaults to undefined|


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

