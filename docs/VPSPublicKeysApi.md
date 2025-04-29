# VPSPublicKeysApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**attachPublicKeyV1**](#attachpublickeyv1) | **POST** /api/vps/v1/public-keys/attach/{virtualMachineId} | Attach public key|
|[**createNewPublicKeyV1**](#createnewpublickeyv1) | **POST** /api/vps/v1/public-keys | Create new public key|
|[**deleteAPublicKeyV1**](#deleteapublickeyv1) | **DELETE** /api/vps/v1/public-keys/{publicKeyId} | Delete a public key|
|[**getPublicKeyListV1**](#getpublickeylistv1) | **GET** /api/vps/v1/public-keys | Get public key list|

# **attachPublicKeyV1**
> VPSV1ActionActionResource attachPublicKeyV1(vPSV1PublicKeyAttachRequest)

This endpoint attaches an existing public keys from your account to a specified virtual machine.  Multiple keys can be attached to a single virtual machine.

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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createNewPublicKeyV1**
> VPSV1PublicKeyPublicKeyResource createNewPublicKeyV1(vPSV1PublicKeyStoreRequest)

This endpoint allows you to add a new public key to your account,  which can then be attached to virtual machine instances for secure access.

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

const { status, data } = await apiInstance.createNewPublicKeyV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAPublicKeyV1**
> CommonSuccessEmptyResource deleteAPublicKeyV1()

This endpoint deletes a public key from your account.   **Deleting public key from account does not remove it from virtual machine** 

### Example

```typescript
import {
    VPSPublicKeysApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPublicKeysApi(configuration);

let publicKeyId: number; //Public Key ID (default to undefined)

const { status, data } = await apiInstance.deleteAPublicKeyV1(
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
|**401** | Unauthenticated |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPublicKeyListV1**
> VPSGetPublicKeyListV1200Response getPublicKeyListV1()

This endpoint retrieves a list of public keys associated with your account.

### Example

```typescript
import {
    VPSPublicKeysApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSPublicKeysApi(configuration);

let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.getPublicKeyListV1(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

