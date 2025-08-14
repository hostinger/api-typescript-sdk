# VPSActionsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getActionDetailsV1**](#getactiondetailsv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/actions/{actionId} | Get action details|
|[**getActionsV1**](#getactionsv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/actions | Get actions|

# **getActionDetailsV1**
> VPSV1ActionActionResource getActionDetailsV1()

Retrieve detailed information about a specific action performed on a specified virtual machine.  Use this endpoint to monitor specific VPS operation status and details.

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

const { status, data } = await apiInstance.getActionDetailsV1(
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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getActionsV1**
> VPSGetActionsV1200Response getActionsV1()

Retrieve actions performed on a specified virtual machine.  Actions are operations or events that have been executed on the virtual machine, such as starting, stopping, or modifying  the machine. This endpoint allows you to view the history of these actions, providing details about each action,  such as the action name, timestamp, and status.  Use this endpoint to view VPS operation history and troubleshoot issues.

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

const { status, data } = await apiInstance.getActionsV1(
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

**VPSGetActionsV1200Response**

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

