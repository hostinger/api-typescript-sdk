# DNSZoneApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteDNSRecordsV1**](#deletednsrecordsv1) | **DELETE** /api/dns/v1/zones/{domain} | Delete DNS records|
|[**getDNSRecordsV1**](#getdnsrecordsv1) | **GET** /api/dns/v1/zones/{domain} | Get DNS records|
|[**resetDNSRecordsV1**](#resetdnsrecordsv1) | **POST** /api/dns/v1/zones/{domain}/reset | Reset DNS records|
|[**updateDNSRecordsV1**](#updatednsrecordsv1) | **PUT** /api/dns/v1/zones/{domain} | Update DNS records|
|[**validateDNSRecordsV1**](#validatednsrecordsv1) | **POST** /api/dns/v1/zones/{domain}/validate | Validate DNS records|

# **deleteDNSRecordsV1**
> CommonSuccessEmptyResource deleteDNSRecordsV1(dNSV1ZoneDestroyRequest)

Delete DNS records for the selected domain.  To filter which records to delete, add the `name` of the record and `type` to the filter.  Multiple filters can be provided with single request.  If you have multiple records with the same name and type, and you want to delete only part of them, refer to the `Update zone records` endpoint.  Use this endpoint to remove specific DNS records from domains.

### Example

```typescript
import {
    DNSZoneApi,
    Configuration,
    DNSV1ZoneDestroyRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSZoneApi(configuration);

let domain: string; //Domain name (default to undefined)
let dNSV1ZoneDestroyRequest: DNSV1ZoneDestroyRequest; //

const { status, data } = await apiInstance.deleteDNSRecordsV1(
    domain,
    dNSV1ZoneDestroyRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **dNSV1ZoneDestroyRequest** | **DNSV1ZoneDestroyRequest**|  | |
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
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getDNSRecordsV1**
> Array<DNSV1ZoneRecordResource> getDNSRecordsV1()

Retrieve DNS zone records for a specific domain.  Use this endpoint to view current DNS configuration for domain management.

### Example

```typescript
import {
    DNSZoneApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSZoneApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDNSRecordsV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**Array<DNSV1ZoneRecordResource>**

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

# **resetDNSRecordsV1**
> CommonSuccessEmptyResource resetDNSRecordsV1(dNSV1ZoneResetRequest)

Reset DNS zone to the default records.  Use this endpoint to restore domain DNS to original configuration.

### Example

```typescript
import {
    DNSZoneApi,
    Configuration,
    DNSV1ZoneResetRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSZoneApi(configuration);

let domain: string; //Domain name (default to undefined)
let dNSV1ZoneResetRequest: DNSV1ZoneResetRequest; //

const { status, data } = await apiInstance.resetDNSRecordsV1(
    domain,
    dNSV1ZoneResetRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **dNSV1ZoneResetRequest** | **DNSV1ZoneResetRequest**|  | |
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
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateDNSRecordsV1**
> CommonSuccessEmptyResource updateDNSRecordsV1(dNSV1ZoneUpdateRequest)

Update DNS records for the selected domain.  Using `overwrite = true` will replace existing records with the provided ones.  Otherwise existing records will be updated and new records will be added.  Use this endpoint to modify domain DNS configuration.

### Example

```typescript
import {
    DNSZoneApi,
    Configuration,
    DNSV1ZoneUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSZoneApi(configuration);

let domain: string; //Domain name (default to undefined)
let dNSV1ZoneUpdateRequest: DNSV1ZoneUpdateRequest; //

const { status, data } = await apiInstance.updateDNSRecordsV1(
    domain,
    dNSV1ZoneUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **dNSV1ZoneUpdateRequest** | **DNSV1ZoneUpdateRequest**|  | |
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
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validateDNSRecordsV1**
> CommonSuccessEmptyResource validateDNSRecordsV1(dNSV1ZoneUpdateRequest)

Validate DNS records prior to update for the selected domain.  If the validation is successful, the response will contain `200 Success` code. If there is validation error, the response will fail with `422 Validation error` code.  Use this endpoint to verify DNS record validity before applying changes.

### Example

```typescript
import {
    DNSZoneApi,
    Configuration,
    DNSV1ZoneUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSZoneApi(configuration);

let domain: string; //Domain name (default to undefined)
let dNSV1ZoneUpdateRequest: DNSV1ZoneUpdateRequest; //

const { status, data } = await apiInstance.validateDNSRecordsV1(
    domain,
    dNSV1ZoneUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **dNSV1ZoneUpdateRequest** | **DNSV1ZoneUpdateRequest**|  | |
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
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

