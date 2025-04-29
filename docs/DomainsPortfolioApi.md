# DomainsPortfolioApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**disableDomainLockV1**](#disabledomainlockv1) | **DELETE** /api/domains/v1/portfolio/{domain}/domain-lock | Disable domain lock|
|[**disablePrivacyProtectionV1**](#disableprivacyprotectionv1) | **DELETE** /api/domains/v1/portfolio/{domain}/privacy-protection | Disable privacy protection|
|[**enableDomainLockV1**](#enabledomainlockv1) | **PUT** /api/domains/v1/portfolio/{domain}/domain-lock | Enable domain lock|
|[**enablePrivacyProtectionV1**](#enableprivacyprotectionv1) | **PUT** /api/domains/v1/portfolio/{domain}/privacy-protection | Enable privacy protection|
|[**getDomainListV1**](#getdomainlistv1) | **GET** /api/domains/v1/portfolio | Get domain list|
|[**getDomainV1**](#getdomainv1) | **GET** /api/domains/v1/portfolio/{domain} | Get domain|
|[**purchaseNewDomainV1**](#purchasenewdomainv1) | **POST** /api/domains/v1/portfolio | Purchase new domain|
|[**updateNameserversV1**](#updatenameserversv1) | **PUT** /api/domains/v1/portfolio/{domain}/nameservers | Update nameservers|

# **disableDomainLockV1**
> CommonSuccessEmptyResource disableDomainLockV1()

This endpoint disables domain lock for the domain. Domain lock needs to be disabled  before transferring the domain to another registrar.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disablePrivacyProtectionV1**
> CommonSuccessEmptyResource disablePrivacyProtectionV1()

This endpoint disables privacy protection for the domain. When privacy protection is disabled, the domain owner\'s personal information is visible in the public WHOIS database.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enableDomainLockV1**
> CommonSuccessEmptyResource enableDomainLockV1()

This endpoint enables domain lock for the domain. When domain lock is enabled,  the domain cannot be transferred to another registrar without first disabling the lock.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enablePrivacyProtectionV1**
> CommonSuccessEmptyResource enablePrivacyProtectionV1()

This endpoint enables privacy protection for the domain. When privacy protection is enabled, the domain owner\'s personal information is hidden from the public WHOIS database.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDomainListV1**
> Array<DomainsV1DomainDomainResource> getDomainListV1()

This endpoint retrieves a list of all domains associated with your account.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDomainV1**
> DomainsV1DomainDomainExtendedResource getDomainV1()

This endpoint retrieves details for specified domain.

### Example

```typescript
import {
    DomainsPortfolioApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsPortfolioApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDomainV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **purchaseNewDomainV1**
> BillingV1OrderOrderResource purchaseNewDomainV1(domainsV1PortfolioPurchaseRequest)

This endpoint purchases and registers new domain. If registration fails, login to hPanel and check the domain registration status.  If no payment method is provided, default will be used.  If no WHOIS information is provided, default for that TLD will be used.  Before making request make sure that WHOIS information for TLD exists.  Some TLDs require `additional_details` to be provided and will be validated before making purchase.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateNameserversV1**
> CommonSuccessEmptyResource updateNameserversV1(domainsV1PortfolioUpdateNameserversRequest)

This endpoint sets the nameservers for a specified domain.  Be aware, that improper nameserver configuration can lead to the domain being unresolvable or unavailable. 

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

const { status, data } = await apiInstance.updateNameserversV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

