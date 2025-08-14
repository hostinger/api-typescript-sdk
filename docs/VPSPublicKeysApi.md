# VPSPublicKeysApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**attachPublicKeyV1**](#attachpublickeyv1) | **POST** /api/vps/v1/public-keys/attach/{virtualMachineId} | Attach public key|
|[**createPublicKeyV1**](#createpublickeyv1) | **POST** /api/vps/v1/public-keys | Create public key|
|[**deletePublicKeyV1**](#deletepublickeyv1) | **DELETE** /api/vps/v1/public-keys/{publicKeyId} | Delete public key|
|[**getPublicKeysV1**](#getpublickeysv1) | **GET** /api/vps/v1/public-keys | Get public keys|

# **attachPublicKeyV1**
> VPSV1ActionActionResource attachPublicKeyV1(vPSV1PublicKeyAttachRequest)

Attach existing public keys from your account to a specified virtual machine.  Multiple keys can be attached to a single virtual machine.  Use this endpoint to enable SSH key authentication for VPS instances.

### Example

```typescript
import {
    VPSPublicKeysApi,
    Configuration,
    VPSV1PublicKeyAttachRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPublicKeysApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1PublicKeyAttachRequest: VPSV1PublicKeyAttachRequest; //

const { status, data } = await apiInstance.attachPublicKeyV1(
    virtualMachineId,
    vPSV1PublicKeyAttachRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1PublicKeyAttachRequest** | **VPSV1PublicKeyAttachRequest**|  | |
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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createPublicKeyV1**
> VPSV1PublicKeyPublicKeyResource createPublicKeyV1(vPSV1PublicKeyStoreRequest)

Add a new public key to your account.  Use this endpoint to register SSH keys for VPS authentication.

### Example

```typescript
import {
    VPSPublicKeysApi,
    Configuration,
    VPSV1PublicKeyStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPublicKeysApi(configuration);

let vPSV1PublicKeyStoreRequest: VPSV1PublicKeyStoreRequest; //

const { status, data } = await apiInstance.createPublicKeyV1(
    vPSV1PublicKeyStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1PublicKeyStoreRequest** | **VPSV1PublicKeyStoreRequest**|  | |


### Return type

**VPSV1PublicKeyPublicKeyResource**

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

# **deletePublicKeyV1**
> CommonSuccessEmptyResource deletePublicKeyV1()

Delete a public key from your account.   **Deleting public key from account does not remove it from virtual machine**          Use this endpoint to remove unused SSH keys from account.

### Example

```typescript
import {
    VPSPublicKeysApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPublicKeysApi(configuration);

let publicKeyId: number; //Public Key ID (default to undefined)

const { status, data } = await apiInstance.deletePublicKeyV1(
    publicKeyId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **publicKeyId** | [**number**] | Public Key ID | defaults to undefined|


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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPublicKeysV1**
> VPSGetPublicKeysV1200Response getPublicKeysV1()

Retrieve public keys associated with your account.  Use this endpoint to view available SSH keys for VPS authentication.

### Example

```typescript
import {
    VPSPublicKeysApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPublicKeysApi(configuration);

let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getPublicKeysV1(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**VPSGetPublicKeysV1200Response**

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

