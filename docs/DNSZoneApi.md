# DNSZoneApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteZoneRecordsV1**](#deletezonerecordsv1) | **DELETE** /api/dns/v1/zones/{domain} | Delete zone records|
|[**getRecordsV1**](#getrecordsv1) | **GET** /api/dns/v1/zones/{domain} | Get records|
|[**resetZoneRecordsV1**](#resetzonerecordsv1) | **POST** /api/dns/v1/zones/{domain}/reset | Reset zone records|
|[**updateZoneRecordsV1**](#updatezonerecordsv1) | **PUT** /api/dns/v1/zones/{domain} | Update zone records|
|[**validateZoneRecordsV1**](#validatezonerecordsv1) | **POST** /api/dns/v1/zones/{domain}/validate | Validate zone records|

# **deleteZoneRecordsV1**
> CommonSuccessEmptyResource deleteZoneRecordsV1(dNSV1ZoneDestroyRequest)

This endpoint deletes DNS records for the selected domain.  To filter which records to delete, add the `name` of the record and `type` to the filter.  Multiple filters can be provided with single request.  If you have multiple records with the same name and type, and you want to delete only part of them, refer to the `Update zone records` endpoint.

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

const { status, data } = await apiInstance.deleteZoneRecordsV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getRecordsV1**
> Array<DNSV1ZoneRecordResource> getRecordsV1()

This endpoint retrieves DNS zone records for a specific domain.

### Example

```typescript
import {
    DNSZoneApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSZoneApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getRecordsV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resetZoneRecordsV1**
> CommonSuccessEmptyResource resetZoneRecordsV1(dNSV1ZoneResetRequest)

This endpoint resets DNS zone to the default records.

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

const { status, data } = await apiInstance.resetZoneRecordsV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateZoneRecordsV1**
> CommonSuccessEmptyResource updateZoneRecordsV1(dNSV1ZoneUpdateRequest)

This endpoint updates DNS records for the selected domain.   Using `overwrite = true` will replace existing records with the provided ones.  Otherwise existing records will be updated and new records will be added.

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

const { status, data } = await apiInstance.updateZoneRecordsV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validateZoneRecordsV1**
> CommonSuccessEmptyResource validateZoneRecordsV1(dNSV1ZoneUpdateRequest)

This endpoint used to validate DNS records prior update for the selected domain.   If the validation is successful, the response will contain `200 Success` code. If there is validation error, the response will fail with `422 Validation error` code.

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

const { status, data } = await apiInstance.validateZoneRecordsV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

