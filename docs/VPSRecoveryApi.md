# VPSRecoveryApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**startRecoveryModeV1**](#startrecoverymodev1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/recovery | Start recovery mode|
|[**stopRecoveryModeV1**](#stoprecoverymodev1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/recovery | Stop recovery mode|

# **startRecoveryModeV1**
> VPSV1ActionActionResource startRecoveryModeV1(vPSV1VirtualMachineRecoveryStartRequest)

This endpoint initiates the recovery mode for a specified virtual machine.  Recovery mode is a special state that allows users to perform system rescue operations,  such as repairing file systems, recovering data, or troubleshooting issues that prevent the virtual machine  from booting normally.   Virtual machine will boot recovery disk image and original disk image will be mounted in `/mnt` directory.

### Example

```typescript
import {
    VPSRecoveryApi,
    Configuration,
    VPSV1VirtualMachineRecoveryStartRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSRecoveryApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineRecoveryStartRequest: VPSV1VirtualMachineRecoveryStartRequest; //

const { status, data } = await apiInstance.startRecoveryModeV1(
    virtualMachineId,
    vPSV1VirtualMachineRecoveryStartRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineRecoveryStartRequest** | **VPSV1VirtualMachineRecoveryStartRequest**|  | |
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

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

# **stopRecoveryModeV1**
> VPSV1ActionActionResource stopRecoveryModeV1()

This endpoint stops the recovery mode for a specified virtual machine.  If virtual machine is not in recovery mode, this operation will fail.

### Example

```typescript
import {
    VPSRecoveryApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSRecoveryApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.stopRecoveryModeV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

