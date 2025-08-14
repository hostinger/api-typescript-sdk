# DNSSnapshotApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getDNSSnapshotListV1**](#getdnssnapshotlistv1) | **GET** /api/dns/v1/snapshots/{domain} | Get DNS snapshot list|
|[**getDNSSnapshotV1**](#getdnssnapshotv1) | **GET** /api/dns/v1/snapshots/{domain}/{snapshotId} | Get DNS snapshot|
|[**restoreDNSSnapshotV1**](#restorednssnapshotv1) | **POST** /api/dns/v1/snapshots/{domain}/{snapshotId}/restore | Restore DNS snapshot|

# **getDNSSnapshotListV1**
> Array<DNSV1SnapshotSnapshotResource> getDNSSnapshotListV1()

Retrieve DNS snapshots for a domain.  Use this endpoint to view available DNS backup points for restoration.

### Example

```typescript
import {
    DNSSnapshotApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSSnapshotApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getDNSSnapshotListV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**Array<DNSV1SnapshotSnapshotResource>**

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

# **getDNSSnapshotV1**
> DNSV1SnapshotSnapshotWithContentResource getDNSSnapshotV1()

Retrieve particular DNS snapshot with contents of DNS zone records.  Use this endpoint to view historical DNS configurations for domains.

### Example

```typescript
import {
    DNSSnapshotApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSSnapshotApi(configuration);

let domain: string; //Domain name (default to undefined)
let snapshotId: number; //Snapshot ID (default to undefined)

const { status, data } = await apiInstance.getDNSSnapshotV1(
    domain,
    snapshotId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **snapshotId** | [**number**] | Snapshot ID | defaults to undefined|


### Return type

**DNSV1SnapshotSnapshotWithContentResource**

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

# **restoreDNSSnapshotV1**
> CommonSuccessEmptyResource restoreDNSSnapshotV1()

Restore DNS zone to the selected snapshot.  Use this endpoint to revert domain DNS to a previous configuration.

### Example

```typescript
import {
    DNSSnapshotApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSSnapshotApi(configuration);

let domain: string; //Domain name (default to undefined)
let snapshotId: number; //Snapshot ID (default to undefined)

const { status, data } = await apiInstance.restoreDNSSnapshotV1(
    domain,
    snapshotId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|
| **snapshotId** | [**number**] | Snapshot ID | defaults to undefined|


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

