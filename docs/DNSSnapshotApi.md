# DNSSnapshotApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getSnapshotListV1**](#getsnapshotlistv1) | **GET** /api/dns/v1/snapshots/{domain} | Get snapshot list|
|[**getSnapshotV1**](#getsnapshotv1) | **GET** /api/dns/v1/snapshots/{domain}/{snapshotId} | Get snapshot|
|[**restoreSnapshotV1**](#restoresnapshotv1) | **POST** /api/dns/v1/snapshots/{domain}/{snapshotId}/restore | Restore snapshot|

# **getSnapshotListV1**
> Array<DNSV1SnapshotSnapshotResource> getSnapshotListV1()

This endpoint retrieves list of DNS snapshots.

### Example

```typescript
import {
    DNSSnapshotApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new DNSSnapshotApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getSnapshotListV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getSnapshotV1**
> DNSV1SnapshotSnapshotWithContentResource getSnapshotV1()

This endpoint retrieves particular DNS snapshot with the contents of DNS zone records.

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

const { status, data } = await apiInstance.getSnapshotV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restoreSnapshotV1**
> CommonSuccessEmptyResource restoreSnapshotV1()

This endpoint restores DNS zone to the selected snapshot.

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

const { status, data } = await apiInstance.restoreSnapshotV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

