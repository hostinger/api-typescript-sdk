# VPSPTRRecordsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createPTRRecordV1**](#createptrrecordv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/ptr/{ipAddressId} | Create PTR record|
|[**deletePTRRecordV1**](#deleteptrrecordv1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/ptr/{ipAddressId} | Delete PTR record|

# **createPTRRecordV1**
> VPSV1ActionActionResource createPTRRecordV1(vPSV1VirtualMachinePTRStoreRequest)

Create or update a PTR (Pointer) record for a specified virtual machine.  Use this endpoint to configure reverse DNS lookup for VPS IP addresses.

### Example

```typescript
import {
    VPSPTRRecordsApi,
    Configuration,
    VPSV1VirtualMachinePTRStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPTRRecordsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let ipAddressId: number; //IP Address ID (default to undefined)
let vPSV1VirtualMachinePTRStoreRequest: VPSV1VirtualMachinePTRStoreRequest; //

const { status, data } = await apiInstance.createPTRRecordV1(
    virtualMachineId,
    ipAddressId,
    vPSV1VirtualMachinePTRStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachinePTRStoreRequest** | **VPSV1VirtualMachinePTRStoreRequest**|  | |
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **ipAddressId** | [**number**] | IP Address ID | defaults to undefined|


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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePTRRecordV1**
> VPSV1ActionActionResource deletePTRRecordV1()

Delete a PTR (Pointer) record for a specified virtual machine.  Once deleted, reverse DNS lookups to the virtual machine\'s IP address will no longer return the previously configured hostname.  Use this endpoint to remove reverse DNS configuration from VPS instances.

### Example

```typescript
import {
    VPSPTRRecordsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPTRRecordsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let ipAddressId: number; //IP Address ID (default to undefined)

const { status, data } = await apiInstance.deletePTRRecordV1(
    virtualMachineId,
    ipAddressId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **ipAddressId** | [**number**] | IP Address ID | defaults to undefined|


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

