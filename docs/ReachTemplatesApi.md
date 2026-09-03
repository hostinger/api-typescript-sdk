# ReachTemplatesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAnEmailTemplateV1**](#createanemailtemplatev1) | **POST** /api/reach/v1/profiles/{profileUuid}/templates | Create an email template|
|[**listEmailTemplatesV1**](#listemailtemplatesv1) | **GET** /api/reach/v1/profiles/{profileUuid}/templates | List email templates|

# **createAnEmailTemplateV1**
> ReachV1TemplatesTemplateResource createAnEmailTemplateV1(reachV1TemplatesStoreRequest)

Create an email template in a profile.  The template holds the HTML body a campaign reuses, so it can be created before any campaign exists. Only the template metadata comes back - keep the returned `uuid` to reference it as the `template_uuid` of a campaign.

### Example

```typescript
import {
    ReachTemplatesApi,
    Configuration,
    ReachV1TemplatesStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTemplatesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1TemplatesStoreRequest: ReachV1TemplatesStoreRequest; //

const { status, data } = await apiInstance.createAnEmailTemplateV1(
    profileUuid,
    reachV1TemplatesStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1TemplatesStoreRequest** | **ReachV1TemplatesStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1TemplatesTemplateResource**

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

# **listEmailTemplatesV1**
> Array<ReachV1TemplatesTemplateResource> listEmailTemplatesV1()

Get a list of the email templates in a profile, most recently updated first.  Templates are the reusable email bodies a campaign is built from. The list is not paginated and only the metadata is returned - the template content itself is not exposed. Use the `uuid` of a template as the `template_uuid` when creating a campaign.

### Example

```typescript
import {
    ReachTemplatesApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTemplatesApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listEmailTemplatesV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1TemplatesTemplateResource>**

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

