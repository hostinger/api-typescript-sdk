# DomainsPortfolioApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**claimFreeDomainV1**](#claimfreedomainv1) | **POST** /api/domains/v1/portfolio/claim | Claim free domain|
|[**completeDomainSetupV1**](#completedomainsetupv1) | **POST** /api/domains/v1/portfolio/{domain}/setup | Complete domain setup|
|[**disableDomainLockV1**](#disabledomainlockv1) | **DELETE** /api/domains/v1/portfolio/{domain}/domain-lock | Disable domain lock|
|[**disablePrivacyProtectionV1**](#disableprivacyprotectionv1) | **DELETE** /api/domains/v1/portfolio/{domain}/privacy-protection | Disable privacy protection|
|[**enableDomainLockV1**](#enabledomainlockv1) | **PUT** /api/domains/v1/portfolio/{domain}/domain-lock | Enable domain lock|
|[**enablePrivacyProtectionV1**](#enableprivacyprotectionv1) | **PUT** /api/domains/v1/portfolio/{domain}/privacy-protection | Enable privacy protection|
|[**getDomainAuthorizationCodeV1**](#getdomainauthorizationcodev1) | **GET** /api/domains/v1/portfolio/{domain}/auth-code | Get domain authorization code|
|[**getDomainDetailsV1**](#getdomaindetailsv1) | **GET** /api/domains/v1/portfolio/{domain} | Get domain details|
|[**getDomainListV1**](#getdomainlistv1) | **GET** /api/domains/v1/portfolio | Get domain list|
|[**getDomainRenewalInformationV1**](#getdomainrenewalinformationv1) | **GET** /api/domains/v1/portfolio/{domain}/renewal | Get domain renewal information|
|[**purchaseNewDomainV1**](#purchasenewdomainv1) | **POST** /api/domains/v1/portfolio | Purchase new domain|
|[**updateDomainNameserversV1**](#updatedomainnameserversv1) | **PUT** /api/domains/v1/portfolio/{domain}/nameservers | Update domain nameservers|

# **claimFreeDomainV1**
> DomainsV1PortfolioClaimResource claimFreeDomainV1(domainsV1PortfolioClaimRequest)

Claim a free domain available on your account and register it.  Unlike purchasing a domain, this consumes a free domain you already have, so no payment method is required.  A successful response means the domain is registered. If registration fails, login to [hPanel](https://hpanel.hostinger.com/) and check domain registration status.  If no WHOIS information is provided, default contact information for that TLD will be used. Before making request, ensure WHOIS information for desired TLD exists in your account.  Some TLDs require `additional_details` to be provided and these will be validated before claiming.  Requests which cannot be fulfilled are rejected with an error code in the response body, for example `2037` when no free domain is available.  Use this endpoint to register a domain using a free domain from your account.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration,
    DomainsV1PortfolioClaimRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domainsV1PortfolioClaimRequest: DomainsV1PortfolioClaimRequest; //

const { status, data } = await apiInstance.claimFreeDomainV1(
    domainsV1PortfolioClaimRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1PortfolioClaimRequest** | **DomainsV1PortfolioClaimRequest**|  | |


### Return type

**DomainsV1PortfolioClaimResource**

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

# **completeDomainSetupV1**
> CommonSuccessEmptyResource completeDomainSetupV1(domainsV1PortfolioSetupRequest)

Register a domain you have already paid for but which has not been set up yet.  Use this endpoint when an order completed without registering the domain, for example when `Purchase new domain` returned `202 Accepted` and the domain was added to your account without being registered, or when an earlier setup attempt failed. No new order is placed and no payment is taken: the subscription you already own is used, for the period you already paid for.  A domain is left awaiting setup when the details needed to register it were missing or invalid as the order completed. Domains ordered elsewhere can be awaiting setup for the same reason. Complete the missing information, then call this endpoint. If the order itself has not completed yet, the domain is not on your account, wait until it appears in `Get domain list`.  If `domain_contacts` is omitted, the default WHOIS profile of that TLD is used for all four roles. The profile must exist and be complete for the TLD, an incomplete profile is the most common reason a domain is left awaiting setup. Create one with `Create WHOIS profile`.  Some TLDs require `additional_details`. These are validated before setup, so a missing or invalid value is rejected without any registration being attempted.  The domain is set up with the default nameservers and without privacy protection. Use `Update domain nameservers` and `Enable privacy protection` afterwards to change either.  A successful response means the setup request was accepted, not that the domain is already registered. Poll `Get domain list` for the outcome, the domain appears in `Get domain details` only once it is registered.  Use this endpoint to finish registering a domain that is awaiting setup on your account.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration,
    DomainsV1PortfolioSetupRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)
let domainsV1PortfolioSetupRequest: DomainsV1PortfolioSetupRequest; //

const { status, data } = await apiInstance.completeDomainSetupV1(
    domain,
    domainsV1PortfolioSetupRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1PortfolioSetupRequest** | **DomainsV1PortfolioSetupRequest**|  | |
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
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disableDomainLockV1**
> CommonSuccessEmptyResource disableDomainLockV1()

Disable domain lock for the domain.  Domain lock needs to be disabled before transferring the domain to another registrar.  Use this endpoint to prepare domains for transfer to other registrars.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.disableDomainLockV1(
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

# **disablePrivacyProtectionV1**
> CommonSuccessEmptyResource disablePrivacyProtectionV1()

Disable privacy protection for the domain.  When privacy protection is disabled, domain owner\'s personal information is visible in public WHOIS database.  Use this endpoint to make domain owner\'s information publicly visible.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.disablePrivacyProtectionV1(
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

# **enableDomainLockV1**
> CommonSuccessEmptyResource enableDomainLockV1()

Enable domain lock for the domain.  When domain lock is enabled, the domain cannot be transferred to another registrar without first disabling the lock.  Use this endpoint to secure domains against unauthorized transfers.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.enableDomainLockV1(
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

# **enablePrivacyProtectionV1**
> CommonSuccessEmptyResource enablePrivacyProtectionV1()

Enable privacy protection for the domain.  When privacy protection is enabled, domain owner\'s personal information is hidden from public WHOIS database.  Use this endpoint to protect domain owner\'s personal information from public view.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.enablePrivacyProtectionV1(
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

# **getDomainAuthorizationCodeV1**
> DomainsV1PortfolioAuthCodeAuthCodeResource getDomainAuthorizationCodeV1()

Retrieve the authorization (EPP) code for a specified domain so it can be transferred away from Hostinger to another registrar.  Requesting a new code invalidates any code retrieved previously.  Use this endpoint to obtain the code required to transfer a domain to another registrar.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDomainAuthorizationCodeV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1PortfolioAuthCodeAuthCodeResource**

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

# **getDomainDetailsV1**
> DomainsV1DomainDomainExtendedResource getDomainDetailsV1()

Retrieve detailed information for specified domain.  Use this endpoint to view comprehensive domain configuration and status.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDomainDetailsV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1DomainDomainExtendedResource**

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

# **getDomainListV1**
> Array<DomainsV1DomainDomainResource> getDomainListV1()

Retrieve all domains associated with your account.  Use this endpoint to view user\'s domain portfolio.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

const { status, data } = await apiInstance.getDomainListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<DomainsV1DomainDomainResource>**

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

# **getDomainRenewalInformationV1**
> DomainsV1PortfolioRenewalRenewalInformationResource getDomainRenewalInformationV1()

Retrieve renewal information for a specified domain, including its status and current expiration date.  Use this endpoint to build renewal automation and expiry monitoring for a single domain.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDomainRenewalInformationV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1PortfolioRenewalRenewalInformationResource**

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

# **purchaseNewDomainV1**
> BillingV1OrderOrderResource purchaseNewDomainV1(domainsV1PortfolioPurchaseRequest)

Purchase and register a new domain name.  If registration fails, login to [hPanel](https://hpanel.hostinger.com/) and check domain registration status.  If no payment method is provided, your default payment method will be used automatically.  If the response is `202 Accepted`, the payment is still being processed and the domain was **not** registered. Once the order completes, register the domain from [hPanel](https://hpanel.hostinger.com/).  If no WHOIS information is provided, default contact information for that TLD will be used. Before making request, ensure WHOIS information for desired TLD exists in your account.  Some TLDs require `additional_details` to be provided and these will be validated before completing purchase.  Use this endpoint to register new domains for users.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration,
    DomainsV1PortfolioPurchaseRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domainsV1PortfolioPurchaseRequest: DomainsV1PortfolioPurchaseRequest; //

const { status, data } = await apiInstance.purchaseNewDomainV1(
    domainsV1PortfolioPurchaseRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1PortfolioPurchaseRequest** | **DomainsV1PortfolioPurchaseRequest**|  | |


### Return type

**BillingV1OrderOrderResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**202** | Payment is being processed, the order will complete asynchronously |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateDomainNameserversV1**
> CommonSuccessEmptyResource updateDomainNameserversV1(domainsV1PortfolioUpdateNameserversRequest)

Set nameservers for a specified domain.  Be aware, that improper nameserver configuration can lead to the domain being unresolvable or unavailable.  Use this endpoint to configure custom DNS hosting for domains.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration,
    DomainsV1PortfolioUpdateNameserversRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)
let domainsV1PortfolioUpdateNameserversRequest: DomainsV1PortfolioUpdateNameserversRequest; //

const { status, data } = await apiInstance.updateDomainNameserversV1(
    domain,
    domainsV1PortfolioUpdateNameserversRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1PortfolioUpdateNameserversRequest** | **DomainsV1PortfolioUpdateNameserversRequest**|  | |
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

