# VPSBackupsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteBackupV1**](#deletebackupv1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/backups/{backupId} | Delete backup|
|[**getBackupListV1**](#getbackuplistv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/backups | Get backup list|
|[**restoreBackupV1**](#restorebackupv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/backups/{backupId}/restore | Restore backup|

# **deleteBackupV1**
> CommonSuccessEmptyResource deleteBackupV1()

This endpoint deletes a specified backup for a virtual machine.

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

const { status, data } = await apiInstance.deleteBackupV1(
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

# **getBackupListV1**
> VPSGetBackupListV1200Response getBackupListV1()

This endpoint retrieves a list of backups for a specified virtual machine.

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

const { status, data } = await apiInstance.getBackupListV1(
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

**VPSGetBackupListV1200Response**

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

# **restoreBackupV1**
> VPSV1ActionActionResource restoreBackupV1()

This endpoint restores a backup for a specified virtual machine.  The system will then initiate the restore process, which may take some time depending on the size of the backup.  **All data on the virtual machine will be overwritten with the data from the backup.**

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

