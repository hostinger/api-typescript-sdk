# DomainsWHOISApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWHOISProfileV1**](#createwhoisprofilev1) | **POST** /api/domains/v1/whois | Create WHOIS profile|
|[**deleteWHOISProfileV1**](#deletewhoisprofilev1) | **DELETE** /api/domains/v1/whois/{whoisId} | Delete WHOIS profile|
|[**getWHOISProfileListV1**](#getwhoisprofilelistv1) | **GET** /api/domains/v1/whois | Get WHOIS profile list|
|[**getWHOISProfileUsageV1**](#getwhoisprofileusagev1) | **GET** /api/domains/v1/whois/{whoisId}/usage | Get WHOIS profile usage|
|[**getWHOISProfileV1**](#getwhoisprofilev1) | **GET** /api/domains/v1/whois/{whoisId} | Get WHOIS profile|

# **createWHOISProfileV1**
> DomainsV1WHOISProfileResource createWHOISProfileV1(domainsV1WHOISStoreRequest)

This endpoint creates WHOIS contact profile.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration,
    DomainsV1WHOISStoreRequest
} from 'hostinger-api-sdk';

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteWHOISProfileV1**
> CommonSuccessEmptyResource deleteWHOISProfileV1()

This endpoint deletes WHOIS contact profile.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from 'hostinger-api-sdk';

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWHOISProfileListV1**
> Array<DomainsV1WHOISProfileResource> getWHOISProfileListV1()

This endpoint retrieves a list of WHOIS contact profiles.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DomainsWHOISApi(configuration);

let tld: string; //Filter by TLD (without trailing dot) (optional) (default to undefined)

const { status, data } = await apiInstance.getWHOISProfileListV1(
    tld
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **tld** | [**string**] | Filter by TLD (without trailing dot) | (optional) defaults to undefined|


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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWHOISProfileUsageV1**
> Array<string> getWHOISProfileUsageV1()

This endpoint retrieves a domain list where provided WHOIS contact profile is used.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from 'hostinger-api-sdk';

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getWHOISProfileV1**
> DomainsV1WHOISProfileResource getWHOISProfileV1()

This endpoint retrieves a WHOIS contact profile.

### Example

```typescript
import {
    DomainsWHOISApi,
    Configuration
} from 'hostinger-api-sdk';

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

