# HostingDomainsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebsiteParkedDomainV1**](#createwebsiteparkeddomainv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/parked-domains | Create website parked domain|
|[**createWebsiteSubdomainV1**](#createwebsitesubdomainv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/subdomains | Create website subdomain|
|[**deleteWebsiteParkedDomainV1**](#deletewebsiteparkeddomainv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/parked-domains/{parkedDomain} | Delete website parked domain|
|[**deleteWebsiteSubdomainV1**](#deletewebsitesubdomainv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/subdomains/{subdomain} | Delete website subdomain|
|[**generateAFreeSubdomainV1**](#generateafreesubdomainv1) | **POST** /api/hosting/v1/domains/free-subdomains | Generate a free subdomain|
|[**listWebsiteParkedDomainsV1**](#listwebsiteparkeddomainsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/parked-domains | List website parked domains|
|[**listWebsiteSubdomainsV1**](#listwebsitesubdomainsv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/subdomains | List website subdomains|
|[**verifyDomainOwnershipV1**](#verifydomainownershipv1) | **POST** /api/hosting/v1/domains/verify-ownership | Verify domain ownership|

# **createWebsiteParkedDomainV1**
> CommonSuccessEmptyResource createWebsiteParkedDomainV1(hostingV1DomainsCreateParkedDomainRequest)

Create a parked or alias domain for the selected website.  Provide a domain name or IP address to park on the website so it serves the same content as the parent domain.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration,
    HostingV1DomainsCreateParkedDomainRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1DomainsCreateParkedDomainRequest: HostingV1DomainsCreateParkedDomainRequest; //

const { status, data } = await apiInstance.createWebsiteParkedDomainV1(
    username,
    domain,
    hostingV1DomainsCreateParkedDomainRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1DomainsCreateParkedDomainRequest** | **HostingV1DomainsCreateParkedDomainRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
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

# **createWebsiteSubdomainV1**
> CommonSuccessEmptyResource createWebsiteSubdomainV1(hostingV1DomainsCreateSubdomainRequest)

Create a new subdomain for the selected website.  Provide a subdomain prefix and, optionally, a custom directory or the website public directory to use as the subdomain root.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration,
    HostingV1DomainsCreateSubdomainRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1DomainsCreateSubdomainRequest: HostingV1DomainsCreateSubdomainRequest; //

const { status, data } = await apiInstance.createWebsiteSubdomainV1(
    username,
    domain,
    hostingV1DomainsCreateSubdomainRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1DomainsCreateSubdomainRequest** | **HostingV1DomainsCreateSubdomainRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
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

# **deleteWebsiteParkedDomainV1**
> CommonSuccessEmptyResource deleteWebsiteParkedDomainV1()

Delete an existing parked or alias domain from the selected website.  Use this endpoint to remove parked domains that are no longer needed.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let parkedDomain: string; // (default to undefined)

const { status, data } = await apiInstance.deleteWebsiteParkedDomainV1(
    username,
    domain,
    parkedDomain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **parkedDomain** | [**string**] |  | defaults to undefined|


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

# **deleteWebsiteSubdomainV1**
> CommonSuccessEmptyResource deleteWebsiteSubdomainV1()

Delete an existing subdomain from the selected website.  Use this endpoint to remove subdomains that are no longer needed.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let subdomain: string; // (default to undefined)

const { status, data } = await apiInstance.deleteWebsiteSubdomainV1(
    username,
    domain,
    subdomain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **subdomain** | [**string**] |  | defaults to undefined|


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

# **generateAFreeSubdomainV1**
> HostingV1DomainsFreeSubdomainResource generateAFreeSubdomainV1()

Generate a unique free subdomain that can be used for hosting services without purchasing custom domains. Free subdomains allow you to start using hosting services immediately and you can always connect a custom domain to your site later.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

const { status, data } = await apiInstance.generateAFreeSubdomainV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**HostingV1DomainsFreeSubdomainResource**

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

# **listWebsiteParkedDomainsV1**
> Array<HostingV1DomainsParkedDomainResource> listWebsiteParkedDomainsV1()

Retrieve all parked or alias domains created under the selected website.  Use this endpoint to inspect parked domain configuration for a specific website, including the parent domain and root directory assigned to each parked domain.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.listWebsiteParkedDomainsV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**Array<HostingV1DomainsParkedDomainResource>**

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

# **listWebsiteSubdomainsV1**
> Array<HostingV1DomainsSubdomainResource> listWebsiteSubdomainsV1()

Retrieve all subdomains created under the selected website.  Use this endpoint to inspect subdomain configuration for a specific website, including the parent domain and root directory assigned to each subdomain.

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.listWebsiteSubdomainsV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**Array<HostingV1DomainsSubdomainResource>**

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

# **verifyDomainOwnershipV1**
> HostingV1DomainsDomainAccessResource verifyDomainOwnershipV1(hostingV1DomainsVerifyOwnershipRequest)

Verify ownership of a single domain and return the verification status.  Use this endpoint to check if a domain is accessible for you before using it for new websites. If the domain is accessible, the response will have `is_accessible: true`. If not, add the given TXT record to your domain\'s DNS records and try verifying again. Keep in mind that it may take up to 10 minutes for new TXT DNS records to propagate.  Skip this verification when using Hostinger\'s free subdomains (*.hostingersite.com).

### Example

```typescript
import {
    HostingDomainsApi,
    Configuration,
    HostingV1DomainsVerifyOwnershipRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDomainsApi(configuration);

let hostingV1DomainsVerifyOwnershipRequest: HostingV1DomainsVerifyOwnershipRequest; //

const { status, data } = await apiInstance.verifyDomainOwnershipV1(
    hostingV1DomainsVerifyOwnershipRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1DomainsVerifyOwnershipRequest** | **HostingV1DomainsVerifyOwnershipRequest**|  | |


### Return type

**HostingV1DomainsDomainAccessResource**

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

