# VPSBackupsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getBackupsV1**](#getbackupsv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/backups | Get backups|
|[**restoreBackupV1**](#restorebackupv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/backups/{backupId}/restore | Restore backup|

# **getBackupsV1**
> VPSGetBackupsV1200Response getBackupsV1()

Retrieve backups for a specified virtual machine.  Use this endpoint to view available backup points for VPS data recovery.

### Example

```typescript
import {
    VPSBackupsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSBackupsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getBackupsV1(
    virtualMachineId,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**VPSGetBackupsV1200Response**

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

# **restoreBackupV1**
> VPSV1ActionActionResource restoreBackupV1()

Restore a backup for a specified virtual machine.  The system will then initiate the restore process, which may take some time depending on the size of the backup.  **All data on the virtual machine will be overwritten with the data from the backup.**  Use this endpoint to recover VPS data from backup points.

### Example

```typescript
import {
    VPSBackupsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSBackupsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let backupId: number; //Backup ID (default to undefined)

const { status, data } = await apiInstance.restoreBackupV1(
    virtualMachineId,
    backupId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **backupId** | [**number**] | Backup ID | defaults to undefined|


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

