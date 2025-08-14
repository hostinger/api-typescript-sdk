# VPSSnapshotsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createSnapshotV1**](#createsnapshotv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/snapshot | Create snapshot|
|[**deleteSnapshotV1**](#deletesnapshotv1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/snapshot | Delete snapshot|
|[**getSnapshotV1**](#getsnapshotv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/snapshot | Get snapshot|
|[**restoreSnapshotV1**](#restoresnapshotv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/snapshot/restore | Restore snapshot|

# **createSnapshotV1**
> VPSV1ActionActionResource createSnapshotV1()

Create a snapshot of a specified virtual machine.  A snapshot captures the state and data of the virtual machine at a specific point in time,  allowing users to restore the virtual machine to that state if needed.  This operation is useful for backup purposes, system recovery,  and testing changes without affecting the current state of the virtual machine.  **Creating new snapshot will overwrite the existing snapshot!**  Use this endpoint to capture VPS state for backup and recovery purposes.

### Example

```typescript
import {
    VPSSnapshotsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSSnapshotsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.createSnapshotV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

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

# **deleteSnapshotV1**
> VPSV1ActionActionResource deleteSnapshotV1()

Delete a snapshot of a specified virtual machine.  Use this endpoint to remove VPS snapshots.

### Example

```typescript
import {
    VPSSnapshotsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSSnapshotsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.deleteSnapshotV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

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

# **getSnapshotV1**
> VPSV1SnapshotSnapshotResource getSnapshotV1()

Retrieve snapshot for a specified virtual machine.  Use this endpoint to view current VPS snapshot information.

### Example

```typescript
import {
    VPSSnapshotsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSSnapshotsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.getSnapshotV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1SnapshotSnapshotResource**

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

# **restoreSnapshotV1**
> VPSV1ActionActionResource restoreSnapshotV1()

Restore a specified virtual machine to a previous state using a snapshot.  Restoring from a snapshot allows users to revert the virtual machine to that state, which is useful for system recovery, undoing changes, or testing.  Use this endpoint to revert VPS instances to previous saved states.

### Example

```typescript
import {
    VPSSnapshotsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSSnapshotsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.restoreSnapshotV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

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

