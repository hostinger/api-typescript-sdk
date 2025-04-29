# VPSVirtualMachineApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAttachedPublicKeysV1**](#getattachedpublickeysv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/public-keys | Get attached public keys|
|[**getMetricsV1**](#getmetricsv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/metrics | Get metrics|
|[**getVirtualMachineListV1**](#getvirtualmachinelistv1) | **GET** /api/vps/v1/virtual-machines | Get virtual machine list|
|[**getVirtualMachineV1**](#getvirtualmachinev1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId} | Get virtual machine|
|[**recreateVirtualMachineV1**](#recreatevirtualmachinev1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/recreate | Recreate virtual machine|
|[**resetHostnameV1**](#resethostnamev1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/hostname | Reset hostname|
|[**restartVirtualMachineV1**](#restartvirtualmachinev1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/restart | Restart virtual machine|
|[**setHostnameV1**](#sethostnamev1) | **PUT** /api/vps/v1/virtual-machines/{virtualMachineId}/hostname | Set hostname|
|[**setNameserversV1**](#setnameserversv1) | **PUT** /api/vps/v1/virtual-machines/{virtualMachineId}/nameservers | Set nameservers|
|[**setPanelPasswordV1**](#setpanelpasswordv1) | **PUT** /api/vps/v1/virtual-machines/{virtualMachineId}/panel-password | Set panel password|
|[**setRootPasswordV1**](#setrootpasswordv1) | **PUT** /api/vps/v1/virtual-machines/{virtualMachineId}/root-password | Set root password|
|[**setupNewVirtualMachineV1**](#setupnewvirtualmachinev1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/setup | Setup new virtual machine|
|[**startVirtualMachineV1**](#startvirtualmachinev1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/start | Start virtual machine|
|[**stopVirtualMachineV1**](#stopvirtualmachinev1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/stop | Stop virtual machine|

# **getAttachedPublicKeysV1**
> VPSGetPublicKeyListV1200Response getAttachedPublicKeysV1()

This endpoint retrieves a list of public keys attached to a specified virtual machine.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getAttachedPublicKeysV1(
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

**VPSGetPublicKeyListV1200Response**

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

# **getMetricsV1**
> VPSV1MetricsMetricsCollection getMetricsV1()

This endpoint retrieves the historical metrics for a specified virtual machine. It includes the following metrics:  - CPU usage - Memory usage - Disk usage - Network usage - Uptime

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let dateFrom: string; //the date-time notation as defined by RFC 3339, section 5.6 (default to undefined)
let dateTo: string; //the date-time notation as defined by RFC 3339, section 5.6 (default to undefined)

const { status, data } = await apiInstance.getMetricsV1(
    virtualMachineId,
    dateFrom,
    dateTo
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **dateFrom** | [**string**] | the date-time notation as defined by RFC 3339, section 5.6 | defaults to undefined|
| **dateTo** | [**string**] | the date-time notation as defined by RFC 3339, section 5.6 | defaults to undefined|


### Return type

**VPSV1MetricsMetricsCollection**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getVirtualMachineListV1**
> Array<VPSV1VirtualMachineVirtualMachineResource> getVirtualMachineListV1()

This endpoint retrieves a list of all available virtual machines.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

const { status, data } = await apiInstance.getVirtualMachineListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<VPSV1VirtualMachineVirtualMachineResource>**

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

# **getVirtualMachineV1**
> VPSV1VirtualMachineVirtualMachineResource getVirtualMachineV1()

This endpoint retrieves detailed information about a specified virtual machine.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.getVirtualMachineV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1VirtualMachineVirtualMachineResource**

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

# **recreateVirtualMachineV1**
> VPSV1ActionActionResource recreateVirtualMachineV1(vPSV1VirtualMachineRecreateRequest)

This endpoint will recreate a virtual machine from scratch.  The recreation process involves reinstalling the operating system and resetting the virtual machine to its initial state. Snapshots, if there are any, will be deleted.  ## Password Requirements Password will be checked against leaked password databases.  Requirements for the password are: - At least 8 characters long - At least one uppercase letter - At least one lowercase letter - At least one number - Is not leaked publicly  **This operation is irreversible and will result in the loss of all data stored on the virtual machine!**

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration,
    VPSV1VirtualMachineRecreateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineRecreateRequest: VPSV1VirtualMachineRecreateRequest; //

const { status, data } = await apiInstance.recreateVirtualMachineV1(
    virtualMachineId,
    vPSV1VirtualMachineRecreateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineRecreateRequest** | **VPSV1VirtualMachineRecreateRequest**|  | |
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

# **resetHostnameV1**
> VPSV1ActionActionResource resetHostnameV1()

This endpoint resets the hostname and PTR record of a specified virtual machine to the default value.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.resetHostnameV1(
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

# **restartVirtualMachineV1**
> VPSV1ActionActionResource restartVirtualMachineV1()

This endpoint restarts a specified virtual machine. This is equivalent to fully stopping and starting the virtual machine. If the virtual machine was stopped, it will be started.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.restartVirtualMachineV1(
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

# **setHostnameV1**
> VPSV1ActionActionResource setHostnameV1(vPSV1VirtualMachineHostnameUpdateRequest)

This endpoint sets the hostname for a specified virtual machine.  Changing hostname does not update PTR record automatically. If you want your virtual machine to be reachable by a hostname,  you need to point your domain A/AAAA records to virtual machine IP as well.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration,
    VPSV1VirtualMachineHostnameUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineHostnameUpdateRequest: VPSV1VirtualMachineHostnameUpdateRequest; //

const { status, data } = await apiInstance.setHostnameV1(
    virtualMachineId,
    vPSV1VirtualMachineHostnameUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineHostnameUpdateRequest** | **VPSV1VirtualMachineHostnameUpdateRequest**|  | |
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

# **setNameserversV1**
> VPSV1ActionActionResource setNameserversV1(vPSV1VirtualMachineNameserversUpdateRequest)

This endpoint sets the nameservers for a specified virtual machine. Be aware, that improper nameserver configuration can lead to the virtual machine being unable to resolve domain names.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration,
    VPSV1VirtualMachineNameserversUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineNameserversUpdateRequest: VPSV1VirtualMachineNameserversUpdateRequest; //

const { status, data } = await apiInstance.setNameserversV1(
    virtualMachineId,
    vPSV1VirtualMachineNameserversUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineNameserversUpdateRequest** | **VPSV1VirtualMachineNameserversUpdateRequest**|  | |
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

# **setPanelPasswordV1**
> VPSV1ActionActionResource setPanelPasswordV1(vPSV1VirtualMachinePanelPasswordUpdateRequest)

This endpoint sets the panel password for a specified virtual machine.  If virtual machine does not use panel OS, the request will still be processed without any effect. Requirements for the password is the same as in the [recreate virtual machine endpoint](/#tag/vps-virtual-machine/POST/api/vps/v1/virtual-machines/{virtualMachineId}/recreate).

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration,
    VPSV1VirtualMachinePanelPasswordUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachinePanelPasswordUpdateRequest: VPSV1VirtualMachinePanelPasswordUpdateRequest; //

const { status, data } = await apiInstance.setPanelPasswordV1(
    virtualMachineId,
    vPSV1VirtualMachinePanelPasswordUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachinePanelPasswordUpdateRequest** | **VPSV1VirtualMachinePanelPasswordUpdateRequest**|  | |
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

# **setRootPasswordV1**
> VPSV1ActionActionResource setRootPasswordV1(vPSV1VirtualMachineRootPasswordUpdateRequest)

This endpoint sets the root password for a specified virtual machine.  Requirements for the password is the same as in the [recreate virtual machine endpoint](/#tag/vps-virtual-machine/POST/api/vps/v1/virtual-machines/{virtualMachineId}/recreate).

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration,
    VPSV1VirtualMachineRootPasswordUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineRootPasswordUpdateRequest: VPSV1VirtualMachineRootPasswordUpdateRequest; //

const { status, data } = await apiInstance.setRootPasswordV1(
    virtualMachineId,
    vPSV1VirtualMachineRootPasswordUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineRootPasswordUpdateRequest** | **VPSV1VirtualMachineRootPasswordUpdateRequest**|  | |
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

# **setupNewVirtualMachineV1**
> VPSV1VirtualMachineVirtualMachineResource setupNewVirtualMachineV1(vPSV1VirtualMachineSetupRequest)

This endpoint will setup newly purchased virtual machine. Such virtual machines has `initial` state.  New virtual machine can be purchased using [`/api/billing/v1/orders`](/#tag/billing-orders/POST/api/billing/v1/orders) endpoint.                        

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration,
    VPSV1VirtualMachineSetupRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineSetupRequest: VPSV1VirtualMachineSetupRequest; //

const { status, data } = await apiInstance.setupNewVirtualMachineV1(
    virtualMachineId,
    vPSV1VirtualMachineSetupRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineSetupRequest** | **VPSV1VirtualMachineSetupRequest**|  | |
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1VirtualMachineVirtualMachineResource**

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

# **startVirtualMachineV1**
> VPSV1ActionActionResource startVirtualMachineV1()

This endpoint starts a specified virtual machine.  If the virtual machine is already running, the request will still be processed without any effect.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.startVirtualMachineV1(
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

# **stopVirtualMachineV1**
> VPSV1ActionActionResource stopVirtualMachineV1()

This endpoint stops a specified virtual machine.  If the virtual machine is already stopped, the request will still be processed without any effect.

### Example

```typescript
import {
    VPSVirtualMachineApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSVirtualMachineApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.stopVirtualMachineV1(
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

