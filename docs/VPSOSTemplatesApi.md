# VPSOSTemplatesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getTemplateDetailsV1**](#gettemplatedetailsv1) | **GET** /api/vps/v1/templates/{templateId} | Get template details|
|[**getTemplatesV1**](#gettemplatesv1) | **GET** /api/vps/v1/templates | Get templates|

# **getTemplateDetailsV1**
> VPSV1TemplateTemplateResource getTemplateDetailsV1()

Retrieve detailed information about a specific OS template for virtual machines.  Use this endpoint to view specific template specifications before deployment.

### Example

```typescript
import {
    VPSOSTemplatesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSOSTemplatesApi(configuration);

let templateId: number; //Template ID (default to undefined)

const { status, data } = await apiInstance.getTemplateDetailsV1(
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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getTemplatesV1**
> Array<VPSV1TemplateTemplateResource> getTemplatesV1()

Retrieve available OS templates for virtual machines.  Use this endpoint to view operating system options before creating or recreating VPS instances.

### Example

```typescript
import {
    VPSOSTemplatesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSOSTemplatesApi(configuration);

const { status, data } = await apiInstance.getTemplatesV1();
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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

