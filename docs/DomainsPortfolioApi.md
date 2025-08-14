# DomainsPortfolioApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**disableDomainLockV1**](#disabledomainlockv1) | **DELETE** /api/domains/v1/portfolio/{domain}/domain-lock | Disable domain lock|
|[**disablePrivacyProtectionV1**](#disableprivacyprotectionv1) | **DELETE** /api/domains/v1/portfolio/{domain}/privacy-protection | Disable privacy protection|
|[**enableDomainLockV1**](#enabledomainlockv1) | **PUT** /api/domains/v1/portfolio/{domain}/domain-lock | Enable domain lock|
|[**enablePrivacyProtectionV1**](#enableprivacyprotectionv1) | **PUT** /api/domains/v1/portfolio/{domain}/privacy-protection | Enable privacy protection|
|[**getDomainDetailsV1**](#getdomaindetailsv1) | **GET** /api/domains/v1/portfolio/{domain} | Get domain details|
|[**getDomainListV1**](#getdomainlistv1) | **GET** /api/domains/v1/portfolio | Get domain list|
|[**purchaseNewDomainV1**](#purchasenewdomainv1) | **POST** /api/domains/v1/portfolio | Purchase new domain|
|[**updateDomainNameserversV1**](#updatedomainnameserversv1) | **PUT** /api/domains/v1/portfolio/{domain}/nameservers | Update domain nameservers|

# **disableDomainLockV1**
> CommonSuccessEmptyResource disableDomainLockV1()

Disable domain lock for the domain.  Domain lock needs to be disabled before transferring the domain to another registrar.  Use this endpoint to prepare domains for transfer to other registrars.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

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

# **getDomainDetailsV1**
> DomainsV1DomainDomainExtendedResource getDomainDetailsV1()

Retrieve detailed information for specified domain.  Use this endpoint to view comprehensive domain configuration and status.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

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

# **purchaseNewDomainV1**
> BillingV1OrderOrderResource purchaseNewDomainV1(domainsV1PortfolioPurchaseRequest)

Purchase and register a new domain name.  If registration fails, login to [hPanel](https://hpanel.hostinger.com/) and check domain registration status.  If no payment method is provided, your default payment method will be used automatically.  If no WHOIS information is provided, default contact information for that TLD will be used.  Before making request, ensure WHOIS information for desired TLD exists in your account.  Some TLDs require `additional_details` to be provided and these will be validated before completing purchase.  Use this endpoint to register new domains for users.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration,
    DomainsV1PortfolioPurchaseRequest
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

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

