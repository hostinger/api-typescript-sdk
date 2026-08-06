# ReachContactFieldsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAContactFieldV1**](#createacontactfieldv1) | **POST** /api/reach/v1/profiles/{profileUuid}/contacts/fields | Create a contact field|
|[**deleteAContactFieldV1**](#deleteacontactfieldv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/contacts/fields/{fieldUuid} | Delete a contact field|
|[**listContactFieldsV1**](#listcontactfieldsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/contacts/fields | List contact fields|
|[**updateAContactFieldV1**](#updateacontactfieldv1) | **PATCH** /api/reach/v1/profiles/{profileUuid}/contacts/fields/{fieldUuid} | Update a contact field|

# **createAContactFieldV1**
> ReachV1ContactsFieldsContactFieldResource createAContactFieldV1(reachV1ContactsFieldsStoreRequest)

Define a new custom contact field in a profile.  The `slug` is derived from the label and, like the field type, cannot be changed later. Use the returned uuid to set values on contacts.

### Example

```typescript
import {
    ReachContactFieldsApi,
    Configuration,
    ReachV1ContactsFieldsStoreRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactFieldsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ContactsFieldsStoreRequest: ReachV1ContactsFieldsStoreRequest; //

const { status, data } = await apiInstance.createAContactFieldV1(
    profileUuid,
    reachV1ContactsFieldsStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsFieldsStoreRequest** | **ReachV1ContactsFieldsStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsFieldsContactFieldResource**

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

# **deleteAContactFieldV1**
> CommonSuccessEmptyResource deleteAContactFieldV1()

Delete a custom contact field.  Every value contacts hold for the field is deleted with it, and for the choice types so are its options. The contacts themselves are not affected.

### Example

```typescript
import {
    ReachContactFieldsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactFieldsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let fieldUuid: string; //Contact field uuid parameter (default to undefined)

const { status, data } = await apiInstance.deleteAContactFieldV1(
    profileUuid,
    fieldUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **fieldUuid** | [**string**] | Contact field uuid parameter | defaults to undefined|


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

# **listContactFieldsV1**
> Array<ReachV1ContactsFieldsContactFieldResource> listContactFieldsV1()

Get the custom contact fields defined in a profile.  Custom fields let you store your own attributes on contacts. The returned uuids are what you pass to the contact update endpoint to set values, and choice fields also list the options available to pick from.

### Example

```typescript
import {
    ReachContactFieldsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactFieldsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listContactFieldsV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1ContactsFieldsContactFieldResource>**

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

# **updateAContactFieldV1**
> ReachV1ContactsFieldsContactFieldResource updateAContactFieldV1(reachV1ContactsFieldsUpdateRequest)

Rename a custom contact field and, for the choice types, replace its option set.  Options carrying a uuid are kept and relabelled, options without one are created, and any existing option left out of the list is deleted along with the values contacts hold for it. The field type and slug cannot be changed.

### Example

```typescript
import {
    ReachContactFieldsApi,
    Configuration,
    ReachV1ContactsFieldsUpdateRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactFieldsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let fieldUuid: string; //Contact field uuid parameter (default to undefined)
let reachV1ContactsFieldsUpdateRequest: ReachV1ContactsFieldsUpdateRequest; //

const { status, data } = await apiInstance.updateAContactFieldV1(
    profileUuid,
    fieldUuid,
    reachV1ContactsFieldsUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsFieldsUpdateRequest** | **ReachV1ContactsFieldsUpdateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **fieldUuid** | [**string**] | Contact field uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsFieldsContactFieldResource**

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

