# ReachFormsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**deleteFormV1**](#deleteformv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid} | Delete form|
|[**getFormDetailsV1**](#getformdetailsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/forms/{formUuid} | Get form details|
|[**listFormsV1**](#listformsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/forms | List forms|

# **deleteFormV1**
> CommonSuccessEmptyResource deleteFormV1()

Permanently delete a form together with its template.  A form that has already captured submissions cannot be deleted, so that the contacts it collected are never silently discarded - pause the form instead to stop it collecting new ones. Views alone do not block deletion.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration
} from 'hostinger-api-sdk';

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

# **getFormDetailsV1**
> ReachV1FormsFormDetailsResource getFormDetailsV1()

Get a single form with the URL of its hosted template and the tags it applies to the contacts it captures.  There is no ready-made embed snippet in the response - either serve the template HTML yourself or build your own embed around the form uuid.

### Example

```typescript
import {
    ReachFormsApi,
    Configuration
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachFormsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listFormsV1(
    profileUuid,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


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

