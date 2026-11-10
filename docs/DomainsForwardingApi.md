# DomainsForwardingApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createDomainForwardingV1**](#createdomainforwardingv1) | **POST** /api/domains/v1/forwarding | Create domain forwarding|
|[**deleteDomainForwardingV1**](#deletedomainforwardingv1) | **DELETE** /api/domains/v1/forwarding/{domain} | Delete domain forwarding|
|[**getDomainForwardingV1**](#getdomainforwardingv1) | **GET** /api/domains/v1/forwarding/{domain} | Get domain forwarding|
|[**updateDomainForwardingV1**](#updatedomainforwardingv1) | **PUT** /api/domains/v1/forwarding/{domain} | Update domain forwarding|

# **createDomainForwardingV1**
> DomainsV1ForwardingForwardingResource createDomainForwardingV1(domainsV1ForwardingStoreRequest)

Create domain forwarding configuration.  Creating a forwarding changes the domain\'s DNS. If the domain does not use Hostinger nameservers, they are switched to Hostinger\'s nameservers automatically, so website, email and other services whose DNS is hosted elsewhere stop working. The root (@) A and AAAA records in the domain\'s Hostinger DNS zone are also replaced with records pointing to Hostinger, even when the domain already uses Hostinger nameservers. The domain\'s current nameservers are returned by the [domain details endpoint](#tag/domains-portfolio); confirm with the user before creating a forwarding on a domain that uses other nameservers. DNS changes can take some time to propagate.  Use this endpoint to set up domain redirects to other URLs.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration,
    DomainsV1ForwardingStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domainsV1ForwardingStoreRequest: DomainsV1ForwardingStoreRequest; //

const { status, data } = await apiInstance.createDomainForwardingV1(
    domainsV1ForwardingStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1ForwardingStoreRequest** | **DomainsV1ForwardingStoreRequest**|  | |


### Return type

**DomainsV1ForwardingForwardingResource**

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

# **deleteDomainForwardingV1**
> CommonSuccessEmptyResource deleteDomainForwardingV1()

Delete domain forwarding data.  Use this endpoint to remove redirect configuration from domains.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.deleteDomainForwardingV1(
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
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDomainForwardingV1**
> DomainsV1ForwardingForwardingResource getDomainForwardingV1()

Retrieve domain forwarding data.  Returns 404 when the domain has no forwarding.  Use this endpoint to view current redirect configuration for domains.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDomainForwardingV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1ForwardingForwardingResource**

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

# **updateDomainForwardingV1**
> DomainsV1ForwardingForwardingResource updateDomainForwardingV1(domainsV1ForwardingUpdateRequest)

Update domain forwarding configuration.  Updating a forwarding changes the domain\'s DNS. If the domain does not use Hostinger nameservers, they are switched to Hostinger\'s nameservers automatically, so website, email and other services whose DNS is hosted elsewhere stop working. The root (@) A and AAAA records in the domain\'s Hostinger DNS zone are also replaced with records pointing to Hostinger, even when the domain already uses Hostinger nameservers. The domain\'s current nameservers are returned by the [domain details endpoint](#tag/domains-portfolio); confirm with the user before updating a forwarding on a domain that uses other nameservers. DNS changes can take some time to propagate.  Use this endpoint to modify existing redirect configuration for domains.

### Example

```typescript
import {
    DomainsForwardingApi,
    Configuration,
    DomainsV1ForwardingUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new DomainsForwardingApi(configuration);

let domain: string; //Domain name (default to undefined)
let domainsV1ForwardingUpdateRequest: DomainsV1ForwardingUpdateRequest; //

const { status, data } = await apiInstance.updateDomainForwardingV1(
    domain,
    domainsV1ForwardingUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domainsV1ForwardingUpdateRequest** | **DomainsV1ForwardingUpdateRequest**|  | |
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**DomainsV1ForwardingForwardingResource**

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

