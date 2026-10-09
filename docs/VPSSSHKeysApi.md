# VPSSSHKeysApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addVirtualMachineSSHKeysV1**](#addvirtualmachinesshkeysv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/ssh-keys | Add virtual machine SSH keys|
|[**listVirtualMachineSSHKeysV1**](#listvirtualmachinesshkeysv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/ssh-keys | List virtual machine SSH keys|
|[**removeVirtualMachineSSHKeysV1**](#removevirtualmachinesshkeysv1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/ssh-keys | Remove virtual machine SSH keys|

# **addVirtualMachineSSHKeysV1**
> Array<VPSV1SshKeySshKeyResource> addVirtualMachineSSHKeysV1(vPSV1SshKeyStoreRequest)

Add one or more SSH public keys to a specified virtual machine.  Keys are added to the `root` user and can be used for passwordless SSH authentication. Returns the complete list of SSH keys currently configured on the virtual machine.  Use this endpoint to enable SSH key authentication for VPS instances.

### Example

```typescript
import {
    VPSSSHKeysApi,
    Configuration,
    VPSV1SshKeyStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new VPSSSHKeysApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1SshKeyStoreRequest: VPSV1SshKeyStoreRequest; //

const { status, data } = await apiInstance.addVirtualMachineSSHKeysV1(
    virtualMachineId,
    vPSV1SshKeyStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1SshKeyStoreRequest** | **VPSV1SshKeyStoreRequest**|  | |
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**Array<VPSV1SshKeySshKeyResource>**

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

# **listVirtualMachineSSHKeysV1**
> Array<VPSV1SshKeySshKeyResource> listVirtualMachineSSHKeysV1()

Retrieve SSH public keys currently configured on a specified virtual machine.  Only keys of the `root` user are listed.  Use this endpoint to view SSH keys that can be used for authentication on VPS instances.

### Example

```typescript
import {
    VPSSSHKeysApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new VPSSSHKeysApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.listVirtualMachineSSHKeysV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**Array<VPSV1SshKeySshKeyResource>**

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

# **removeVirtualMachineSSHKeysV1**
> Array<VPSV1SshKeySshKeyResource> removeVirtualMachineSSHKeysV1(vPSV1SshKeyDestroyRequest)

Remove one or more SSH public keys from a specified virtual machine.  Removed keys can no longer be used to authenticate via SSH as the `root` user. Returns the remaining list of SSH keys configured on the virtual machine.  Use this endpoint to revoke SSH key access to VPS instances.

### Example

```typescript
import {
    VPSSSHKeysApi,
    Configuration,
    VPSV1SshKeyDestroyRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new VPSSSHKeysApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1SshKeyDestroyRequest: VPSV1SshKeyDestroyRequest; //

const { status, data } = await apiInstance.removeVirtualMachineSSHKeysV1(
    virtualMachineId,
    vPSV1SshKeyDestroyRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1SshKeyDestroyRequest** | **VPSV1SshKeyDestroyRequest**|  | |
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**Array<VPSV1SshKeySshKeyResource>**

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

