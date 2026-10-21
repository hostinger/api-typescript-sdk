# ReachFormsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**addFormSubmitterTagsV1**](#addformsubmittertagsv1) | **POST** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid}/tags | Add form submitter tags|
|[**createFormV1**](#createformv1) | **POST** /api/reach/v1/profiles/{profileUuid}/forms | Create form|
|[**deleteFormV1**](#deleteformv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid} | Delete form|
|[**duplicateFormV1**](#duplicateformv1) | **POST** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid}/duplicate | Duplicate form|
|[**getFormDetailsV1**](#getformdetailsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid} | Get form details|
|[**listFormsV1**](#listformsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/forms | List forms|
|[**removeFormSubmitterTagV1**](#removeformsubmittertagv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid}/tags | Remove form submitter tag|
|[**updateFormTemplateV1**](#updateformtemplatev1) | **PATCH** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid}/template | Update form template|
|[**updateFormV1**](#updateformv1) | **PATCH** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid} | Update form|

# **addFormSubmitterTagsV1**
> CommonSuccessEmptyResource addFormSubmitterTagsV1(reachV1FormsAssignTagsRequest)

Add tags to a form so that every contact who submits it from now on receives them.  A tag the form already has is skipped; an unknown tag is rejected. Contacts who submitted earlier are not tagged.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration,
    ReachV1FormsAssignTagsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)
let reachV1FormsAssignTagsRequest: ReachV1FormsAssignTagsRequest; //

const { status, data } = await apiInstance.addFormSubmitterTagsV1(
    profileUuid,
    formUuid,
    reachV1FormsAssignTagsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1FormsAssignTagsRequest** | **ReachV1FormsAssignTagsRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **createFormV1**
> ReachV1FormsFormResource createFormV1(reachV1FormsStoreRequest)

Create an empty draft form.  Reach also adds an automatic `form:{name}` tag that every submitter receives. A draft has no design and is not reachable by visitors: save a design with the update form template operation, then take the form live by setting its status to `active`. Creating a form does not consume AI credits.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration,
    ReachV1FormsStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1FormsStoreRequest: ReachV1FormsStoreRequest; //

const { status, data } = await apiInstance.createFormV1(
    profileUuid,
    reachV1FormsStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1FormsStoreRequest** | **ReachV1FormsStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1FormsFormResource**

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

# **deleteFormV1**
> CommonSuccessEmptyResource deleteFormV1()

Permanently delete a form together with its template.  A form that has already captured submissions cannot be deleted, so that the contacts it collected are never silently discarded - pause the form instead to stop it collecting new ones. Views alone do not block deletion.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)

const { status, data } = await apiInstance.deleteFormV1(
    profileUuid,
    formUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


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
|**409** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **duplicateFormV1**
> ReachV1FormsFormResource duplicateFormV1()

Copy a form into a new draft form with the same name and design.  The copy shares the source\'s automatic `form:{name}` tag; other submitter tags are not copied. The copy is not live until its status is set to `active`.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)

const { status, data } = await apiInstance.duplicateFormV1(
    profileUuid,
    formUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


### Return type

**ReachV1FormsFormResource**

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

# **getFormDetailsV1**
> ReachV1FormsFormDetailsResource getFormDetailsV1()

Get a single form with the URL of its hosted template and the tags it applies to the contacts it captures.  There is no ready-made embed snippet in the response - either serve the template HTML yourself or build your own embed around the form uuid.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)

const { status, data } = await apiInstance.getFormDetailsV1(
    profileUuid,
    formUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


### Return type

**ReachV1FormsFormDetailsResource**

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

# **listFormsV1**
> ReachListFormsV1200Response listFormsV1()

Get a paginated list of the signup forms in a profile.  Each form carries a reference to the template that renders it. Get the form details for a directly usable template URL and for the tags the form puts on the contacts it captures.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let status: 'active' | 'paused' | 'draft'; //Return only forms with this status. (optional) (default to undefined)

const { status, data } = await apiInstance.listFormsV1(
    profileUuid,
    page,
    perPage,
    status
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **status** | [**&#39;active&#39; | &#39;paused&#39; | &#39;draft&#39;**]**Array<&#39;active&#39; &#124; &#39;paused&#39; &#124; &#39;draft&#39;>** | Return only forms with this status. | (optional) defaults to undefined|


### Return type

**ReachListFormsV1200Response**

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

# **removeFormSubmitterTagV1**
> CommonSuccessEmptyResource removeFormSubmitterTagV1(reachV1FormsRemoveTagRequest)

Stop a form from applying a tag to its future submitters.  Succeeds also when the form did not have the tag. Contacts who already received the tag keep it, and the tag itself is not deleted. The automatic `form:{name}` tag cannot be removed and is rejected with a conflict.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration,
    ReachV1FormsRemoveTagRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)
let reachV1FormsRemoveTagRequest: ReachV1FormsRemoveTagRequest; //

const { status, data } = await apiInstance.removeFormSubmitterTagV1(
    profileUuid,
    formUuid,
    reachV1FormsRemoveTagRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1FormsRemoveTagRequest** | **ReachV1FormsRemoveTagRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


### Return type

**CommonSuccessEmptyResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success empty response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**409** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateFormTemplateV1**
> ReachV1FormsFormTemplateVersionResource updateFormTemplateV1(reachV1FormsUpdateTemplateRequest)

Save `content` as the latest design of a form and return the stored version.  The HTML is sanitized and, unless the plan allows removing it, the Reach signature is added. Visitors submit the form with an `email` field (required) and optional `name`, `surname` and `phone`. After sanitizing, the design must contain a form container (`data-reach-form`), an email input (`data-reach-field=\"email\"`) and a submit button (`data-reach-submit`); otherwise the request fails with `422` and `errors.content` lists `missing_form_container`, `missing_email_field` and/or `missing_submit_button`.  A `draft` or `paused` form stays unreachable until its status is set to `active`, which publishes this design. On a form that is already `active` the saved design is not public until the form is paused and set to `active` again. Saving a design does not consume AI credits.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration,
    ReachV1FormsUpdateTemplateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)
let reachV1FormsUpdateTemplateRequest: ReachV1FormsUpdateTemplateRequest; //

const { status, data } = await apiInstance.updateFormTemplateV1(
    profileUuid,
    formUuid,
    reachV1FormsUpdateTemplateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1FormsUpdateTemplateRequest** | **ReachV1FormsUpdateTemplateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


### Return type

**ReachV1FormsFormTemplateVersionResource**

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

# **updateFormV1**
> ReachV1FormsFormResource updateFormV1(reachV1FormsUpdateRequest)

Rename a form and/or change its status.  Setting a `draft` or `paused` form to `active` takes it live: its latest saved design is published and visitors can submit it. `paused` and `draft` stop the form from accepting submissions. A form is not reachable by visitors until it is taken live. Design changes saved while the form is already `active` stay unpublished until the form is paused and set to `active` again. Renaming does not rename the automatic `form:{name}` tag.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration,
    ReachV1FormsUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let formUuid: string; //Form uuid parameter (default to undefined)
let reachV1FormsUpdateRequest: ReachV1FormsUpdateRequest; //

const { status, data } = await apiInstance.updateFormV1(
    profileUuid,
    formUuid,
    reachV1FormsUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1FormsUpdateRequest** | **ReachV1FormsUpdateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **formUuid** | [**string**] | Form uuid parameter | defaults to undefined|


### Return type

**ReachV1FormsFormResource**

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

