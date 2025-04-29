# VPSActionsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getActionListV1**](#getactionlistv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/actions | Get action list|
|[**getActionV1**](#getactionv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/actions/{actionId} | Get action|

# **getActionListV1**
> VPSGetActionListV1200Response getActionListV1()

This endpoint retrieves a list of actions performed on a specified virtual machine.  Actions are operations or events that have been executed on the virtual machine, such as starting, stopping, or modifying  the machine. This endpoint allows you to view the history of these actions, providing details about each action,  such as the action name, timestamp, and status.

### Example

```typescript
import {
    VPSActionsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSActionsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getActionListV1(
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

**VPSGetActionListV1200Response**

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

# **getActionV1**
> VPSV1ActionActionResource getActionV1()

This endpoint retrieves details of a specific action performed on a specified virtual machine.   This endpoint allows you to view detailed information about a particular action, including the action name, timestamp, and status.

### Example

```typescript
import {
    VPSActionsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSActionsApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let actionId: number; //Action ID (default to undefined)

const { status, data } = await apiInstance.getActionV1(
    virtualMachineId,
    actionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **actionId** | [**number**] | Action ID | defaults to undefined|


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

