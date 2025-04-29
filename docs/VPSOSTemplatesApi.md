# VPSOSTemplatesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getTemplateListV1**](#gettemplatelistv1) | **GET** /api/vps/v1/templates | Get template list|
|[**getTemplateV1**](#gettemplatev1) | **GET** /api/vps/v1/templates/{templateId} | Get template|

# **getTemplateListV1**
> Array<VPSV1TemplateTemplateResource> getTemplateListV1()

This endpoint retrieves a list of available OS templates for virtual machines.

### Example

```typescript
import {
    VPSOSTemplatesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSOSTemplatesApi(configuration);

const { status, data } = await apiInstance.getTemplateListV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<VPSV1TemplateTemplateResource>**

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

# **getTemplateV1**
> VPSV1TemplateTemplateResource getTemplateV1()

This endpoint retrieves details of a specific OS template for virtual machines.

### Example

```typescript
import {
    VPSOSTemplatesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSOSTemplatesApi(configuration);

let templateId: number; //Template ID (default to undefined)

const { status, data } = await apiInstance.getTemplateV1(
    templateId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **templateId** | [**number**] | Template ID | defaults to undefined|


### Return type

**VPSV1TemplateTemplateResource**

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

