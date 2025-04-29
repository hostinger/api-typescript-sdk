# VPSFirewallApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**activateFirewallV1**](#activatefirewallv1) | **POST** /api/vps/v1/firewall/{firewallId}/activate/{virtualMachineId} | Activate firewall|
|[**createFirewallRuleV1**](#createfirewallrulev1) | **POST** /api/vps/v1/firewall/{firewallId}/rules | Create firewall rule|
|[**createNewFirewallV1**](#createnewfirewallv1) | **POST** /api/vps/v1/firewall | Create new firewall|
|[**deactivateFirewallV1**](#deactivatefirewallv1) | **POST** /api/vps/v1/firewall/{firewallId}/deactivate/{virtualMachineId} | Deactivate firewall|
|[**deleteFirewallRuleV1**](#deletefirewallrulev1) | **DELETE** /api/vps/v1/firewall/{firewallId}/rules/{ruleId} | Delete firewall rule|
|[**deleteFirewallV1**](#deletefirewallv1) | **DELETE** /api/vps/v1/firewall/{firewallId} | Delete firewall|
|[**getFirewallListV1**](#getfirewalllistv1) | **GET** /api/vps/v1/firewall | Get firewall list|
|[**getFirewallV1**](#getfirewallv1) | **GET** /api/vps/v1/firewall/{firewallId} | Get firewall|
|[**syncFirewallV1**](#syncfirewallv1) | **POST** /api/vps/v1/firewall/{firewallId}/sync/{virtualMachineId} | Sync firewall|
|[**updateFirewallRuleV1**](#updatefirewallrulev1) | **PUT** /api/vps/v1/firewall/{firewallId}/rules/{ruleId} | Update firewall rule|

# **activateFirewallV1**
> VPSV1ActionActionResource activateFirewallV1()

This endpoint activates a firewall for a specified virtual machine.   Only one firewall can be active for a virtual machine at a time.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)
let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.activateFirewallV1(
    firewallId,
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|
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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createFirewallRuleV1**
> VPSV1FirewallFirewallRuleResource createFirewallRuleV1(vPSV1FirewallRulesStoreRequest)

This endpoint creates new firewall rule from a specified firewall.  By default, the firewall drops all incoming traffic, which means you must add accept rules for all ports you want to use.  Any virtual machine that has this firewall activated will loose sync with the firewall and will have to be synced again manually.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration,
    VPSV1FirewallRulesStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)
let vPSV1FirewallRulesStoreRequest: VPSV1FirewallRulesStoreRequest; //

const { status, data } = await apiInstance.createFirewallRuleV1(
    firewallId,
    vPSV1FirewallRulesStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1FirewallRulesStoreRequest** | **VPSV1FirewallRulesStoreRequest**|  | |
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|


### Return type

**VPSV1FirewallFirewallRuleResource**

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

# **createNewFirewallV1**
> VPSV1FirewallFirewallResource createNewFirewallV1(vPSV1FirewallStoreRequest)

This endpoint creates a new firewall.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration,
    VPSV1FirewallStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let vPSV1FirewallStoreRequest: VPSV1FirewallStoreRequest; //

const { status, data } = await apiInstance.createNewFirewallV1(
    vPSV1FirewallStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1FirewallStoreRequest** | **VPSV1FirewallStoreRequest**|  | |


### Return type

**VPSV1FirewallFirewallResource**

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

# **deactivateFirewallV1**
> VPSV1ActionActionResource deactivateFirewallV1()

This endpoint deactivates a firewall for a specified virtual machine.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)
let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.deactivateFirewallV1(
    firewallId,
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|
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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteFirewallRuleV1**
> CommonSuccessEmptyResource deleteFirewallRuleV1()

This endpoint deletes a specific firewall rule from a specified firewall.  Any virtual machine that has this firewall activated will loose sync with the firewall and will have to be synced again manually.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)
let ruleId: number; //Firewall Rule ID (default to undefined)

const { status, data } = await apiInstance.deleteFirewallRuleV1(
    firewallId,
    ruleId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|
| **ruleId** | [**number**] | Firewall Rule ID | defaults to undefined|


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

# **deleteFirewallV1**
> CommonSuccessEmptyResource deleteFirewallV1()

This endpoint deletes a specified firewall.   Any virtual machine that has this firewall activated will automatically have it deactivated.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)

const { status, data } = await apiInstance.deleteFirewallV1(
    firewallId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|


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

# **getFirewallListV1**
> VPSGetFirewallListV1200Response getFirewallListV1()

This endpoint retrieves a list of all firewalls available.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getFirewallListV1(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**VPSGetFirewallListV1200Response**

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

# **getFirewallV1**
> VPSV1FirewallFirewallResource getFirewallV1()

This endpoint retrieves firewall by its ID and rules associated with it.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)

const { status, data } = await apiInstance.getFirewallV1(
    firewallId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|


### Return type

**VPSV1FirewallFirewallResource**

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

# **syncFirewallV1**
> VPSV1ActionActionResource syncFirewallV1()

This endpoint syncs a firewall for a specified virtual machine.  Firewall can loose sync with virtual machine if the firewall has new rules added, removed or updated.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)
let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.syncFirewallV1(
    firewallId,
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|
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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateFirewallRuleV1**
> VPSV1FirewallFirewallRuleResource updateFirewallRuleV1(vPSV1FirewallRulesStoreRequest)

This endpoint updates a specific firewall rule from a specified firewall.  Any virtual machine that has this firewall activated will loose sync with the firewall and will have to be synced again manually.

### Example

```typescript
import {
    VPSFirewallApi,
    Configuration,
    VPSV1FirewallRulesStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSFirewallApi(configuration);

let firewallId: number; //Firewall ID (default to undefined)
let ruleId: number; //Firewall Rule ID (default to undefined)
let vPSV1FirewallRulesStoreRequest: VPSV1FirewallRulesStoreRequest; //

const { status, data } = await apiInstance.updateFirewallRuleV1(
    firewallId,
    ruleId,
    vPSV1FirewallRulesStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1FirewallRulesStoreRequest** | **VPSV1FirewallRulesStoreRequest**|  | |
| **firewallId** | [**number**] | Firewall ID | defaults to undefined|
| **ruleId** | [**number**] | Firewall Rule ID | defaults to undefined|


### Return type

**VPSV1FirewallFirewallRuleResource**

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

