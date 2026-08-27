# ReachContactsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createANewContactV1**](#createanewcontactv1) | **POST** /api/reach/v1/contacts | Create a new contact|
|[**createContactsInBulkV1**](#createcontactsinbulkv1) | **POST** /api/reach/v1/profiles/{profileUuid}/contacts/bulk | Create contacts in bulk|
|[**createNewContactsV1**](#createnewcontactsv1) | **POST** /api/reach/v1/profiles/{profileUuid}/contacts | Create new contacts|
|[**deleteAContactV1**](#deleteacontactv1) | **DELETE** /api/reach/v1/contacts/{uuid} | Delete a contact|
|[**deleteAProfileContactV1**](#deleteaprofilecontactv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/contacts/{contactUuid} | Delete a profile contact|
|[**getContactDetailsV1**](#getcontactdetailsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/contacts/{contactUuid} | Get contact details|
|[**listContactGroupsV1**](#listcontactgroupsv1) | **GET** /api/reach/v1/contacts/groups | List contact groups|
|[**listContactsV1**](#listcontactsv1) | **GET** /api/reach/v1/contacts | List contacts|
|[**listProfileContactsV1**](#listprofilecontactsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/contacts | List profile contacts|
|[**updateAContactV1**](#updateacontactv1) | **PATCH** /api/reach/v1/profiles/{profileUuid}/contacts/{contactUuid} | Update a contact|

# **createANewContactV1**
> CommonSuccessEmptyResource createANewContactV1(reachV1ContactsStoreRequest)

Create a new contact in the email marketing system.  This endpoint allows you to create a new contact with basic information like name, email, and surname.  If double opt-in is enabled, the contact will be created with a pending status and a confirmation email will be sent.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration,
    ReachV1ContactsStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let reachV1ContactsStoreRequest: ReachV1ContactsStoreRequest; //

const { status, data } = await apiInstance.createANewContactV1(
    reachV1ContactsStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsStoreRequest** | **ReachV1ContactsStoreRequest**|  | |


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

# **createContactsInBulkV1**
> CommonSuccessEmptyResource createContactsInBulkV1(reachV1ContactsBulkStoreRequest)

Create many contacts in a profile in a single call.  The contacts are imported in the background, so a success response means the import was accepted rather than finished. Contacts whose email already exists in the profile are left as they are. If double opt-in is enabled, new contacts start off pending and are sent a confirmation email.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration,
    ReachV1ContactsBulkStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ContactsBulkStoreRequest: ReachV1ContactsBulkStoreRequest; //

const { status, data } = await apiInstance.createContactsInBulkV1(
    profileUuid,
    reachV1ContactsBulkStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsBulkStoreRequest** | **ReachV1ContactsBulkStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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

# **createNewContactsV1**
> CommonSuccessEmptyResource createNewContactsV1(reachV1ContactsStoreRequest)

Create a new contact in the email marketing system.  This endpoint allows you to create a new contact with basic information like name, email, and surname.  If double opt-in is enabled, the contact will be created with a pending status and a confirmation email will be sent.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration,
    ReachV1ContactsStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ContactsStoreRequest: ReachV1ContactsStoreRequest; //

const { status, data } = await apiInstance.createNewContactsV1(
    profileUuid,
    reachV1ContactsStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsStoreRequest** | **ReachV1ContactsStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


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

# **deleteAContactV1**
> CommonSuccessEmptyResource deleteAContactV1()

Delete a contact with the specified UUID.  This endpoint permanently removes a contact from the email marketing system.  **Deprecated.** This endpoint cannot target a profile, so it always falls back to the client\'s default profile and cannot delete contacts of any other profile. Use `DELETE /api/reach/v1/profiles/{profileUuid}/contacts/{contactUuid}` instead.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let uuid: string; //UUID of the contact to delete (default to undefined)

const { status, data } = await apiInstance.deleteAContactV1(
    uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **uuid** | [**string**] | UUID of the contact to delete | defaults to undefined|


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
|**200** | Success response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteAProfileContactV1**
> CommonSuccessEmptyResource deleteAProfileContactV1()

Permanently delete a contact from a profile.  The contact is removed together with its custom field values and tag assignments.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let contactUuid: string; //Contact uuid parameter (default to undefined)

const { status, data } = await apiInstance.deleteAProfileContactV1(
    profileUuid,
    contactUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **contactUuid** | [**string**] | Contact uuid parameter | defaults to undefined|


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

# **getContactDetailsV1**
> ReachV1ContactsContactDetailsResource getContactDetailsV1()

Get the full details of a single contact.  Alongside the contact\'s own attributes this returns the tags assigned to it and the values it holds for the profile\'s custom contact fields.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let contactUuid: string; //Contact uuid parameter (default to undefined)

const { status, data } = await apiInstance.getContactDetailsV1(
    profileUuid,
    contactUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **contactUuid** | [**string**] | Contact uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsContactDetailsResource**

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

# **listContactGroupsV1**
> Array<ReachV1ContactsGroupsContactGroupResource> listContactGroupsV1()

Get a list of all contact groups.  This endpoint returns a list of contact groups that can be used to organize contacts.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

const { status, data } = await apiInstance.listContactGroupsV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<ReachV1ContactsGroupsContactGroupResource>**

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

# **listContactsV1**
> ReachListContactsV1200Response listContactsV1()

Get a list of contacts, optionally filtered by group and subscription status.  This endpoint returns a paginated list of contacts with their basic information. You can filter contacts by group UUID and subscription status.  **Deprecated.** This endpoint cannot target a profile, so it always falls back to the client\'s default profile and cannot list contacts of any other profile. Use `GET /api/reach/v1/profiles/{profileUuid}/contacts` instead, which also replaces the group filter with a tag filter.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let groupUuid: string; //Filter contacts by group UUID (optional) (default to undefined)
let subscriptionStatus: 'subscribed' | 'unsubscribed' | 'confirmed' | 'pending'; //Filter contacts by subscription status (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)

const { status, data } = await apiInstance.listContactsV1(
    groupUuid,
    subscriptionStatus,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **groupUuid** | [**string**] | Filter contacts by group UUID | (optional) defaults to undefined|
| **subscriptionStatus** | [**&#39;subscribed&#39; | &#39;unsubscribed&#39; | &#39;confirmed&#39; | &#39;pending&#39;**]**Array<&#39;subscribed&#39; &#124; &#39;unsubscribed&#39; &#124; &#39;confirmed&#39; &#124; &#39;pending&#39;>** | Filter contacts by subscription status | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|


### Return type

**ReachListContactsV1200Response**

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

# **listProfileContactsV1**
> ReachListProfileContactsV1200Response listProfileContactsV1()

Get a paginated list of contacts belonging to a profile.  Contacts can be filtered by subscription status, by tag, and by an email search term. The `meta.total` field of the response is the number of contacts matching the filters, so calling this endpoint without filters gives the profile\'s total contact count.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let subscriptionStatus: 'subscribed' | 'unsubscribed' | 'confirmed' | 'pending'; //Filter contacts by subscription status (optional) (default to undefined)
let tagUuid: string; //Filter contacts by tag UUID (optional) (default to undefined)
let search: string; //Search contacts by email (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listProfileContactsV1(
    profileUuid,
    subscriptionStatus,
    tagUuid,
    search,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **subscriptionStatus** | [**&#39;subscribed&#39; | &#39;unsubscribed&#39; | &#39;confirmed&#39; | &#39;pending&#39;**]**Array<&#39;subscribed&#39; &#124; &#39;unsubscribed&#39; &#124; &#39;confirmed&#39; &#124; &#39;pending&#39;>** | Filter contacts by subscription status | (optional) defaults to undefined|
| **tagUuid** | [**string**] | Filter contacts by tag UUID | (optional) defaults to undefined|
| **search** | [**string**] | Search contacts by email | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**ReachListProfileContactsV1200Response**

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

# **updateAContactV1**
> ReachV1ContactsProfileContactUpdateResource updateAContactV1(reachV1ContactsUpdateRequest)

Update a contact\'s attributes and custom field values.  Only the properties present in the request body are changed, so a partial body is enough to change a single attribute. Sending a property as `null` clears it.  The response carries the contact\'s core attributes. Read back its tags, custom field values, source and note with `GET /api/reach/v1/profiles/{profileUuid}/contacts/{contactUuid}`.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration,
    ReachV1ContactsUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let contactUuid: string; //Contact uuid parameter (default to undefined)
let reachV1ContactsUpdateRequest: ReachV1ContactsUpdateRequest; //

const { status, data } = await apiInstance.updateAContactV1(
    profileUuid,
    contactUuid,
    reachV1ContactsUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsUpdateRequest** | **ReachV1ContactsUpdateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **contactUuid** | [**string**] | Contact uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsProfileContactUpdateResource**

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

