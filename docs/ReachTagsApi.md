# ReachTagsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**assignAContactToATagV1**](#assignacontacttoatagv1) | **POST** /api/reach/v1/profiles/{profileUuid}/tags/{tagUuid}/contacts/{contactUuid} | Assign a contact to a tag|
|[**assignContactsToATagV1**](#assigncontactstoatagv1) | **POST** /api/reach/v1/profiles/{profileUuid}/tags/{tagUuid}/contacts | Assign contacts to a tag|
|[**createOrFindTagsV1**](#createorfindtagsv1) | **POST** /api/reach/v1/profiles/{profileUuid}/tags | Create or find tags|
|[**deleteATagV1**](#deleteatagv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/tags/{tagUuid} | Delete a tag|
|[**listProfileTagsV1**](#listprofiletagsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/tags | List profile tags|
|[**removeAContactFromATagV1**](#removeacontactfromatagv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/tags/{tagUuid}/contacts/{contactUuid} | Remove a contact from a tag|
|[**removeContactsFromATagV1**](#removecontactsfromatagv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/tags/{tagUuid}/contacts | Remove contacts from a tag|
|[**renameATagV1**](#renameatagv1) | **PATCH** /api/reach/v1/profiles/{profileUuid}/tags/{tagUuid} | Rename a tag|

# **assignAContactToATagV1**
> ReachV1ContactsTagsTagResource assignAContactToATagV1()

Assign a tag to a single contact.  Unlike the bulk endpoint this is applied immediately rather than queued. Assigning a tag the contact already carries succeeds without duplicating it.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let tagUuid: string; //Tag uuid parameter (default to undefined)
let contactUuid: string; //Contact uuid parameter (default to undefined)

const { status, data } = await apiInstance.assignAContactToATagV1(
    profileUuid,
    tagUuid,
    contactUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **tagUuid** | [**string**] | Tag uuid parameter | defaults to undefined|
| **contactUuid** | [**string**] | Contact uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsTagsTagResource**

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

# **assignContactsToATagV1**
> CommonSuccessEmptyResource assignContactsToATagV1(reachV1ContactsTagsManageContactsRequest)

Assign a tag to many contacts at once.  Pass `contact_uuids` to target specific contacts, or `all_contacts` to target every contact in the profile. The work is queued, so a success response means it was accepted rather than finished. Contacts that already carry the tag are left alone.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration,
    ReachV1ContactsTagsManageContactsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let tagUuid: string; //Tag uuid parameter (default to undefined)
let reachV1ContactsTagsManageContactsRequest: ReachV1ContactsTagsManageContactsRequest; //

const { status, data } = await apiInstance.assignContactsToATagV1(
    profileUuid,
    tagUuid,
    reachV1ContactsTagsManageContactsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsTagsManageContactsRequest** | **ReachV1ContactsTagsManageContactsRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **tagUuid** | [**string**] | Tag uuid parameter | defaults to undefined|


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

# **createOrFindTagsV1**
> Array<ReachV1ContactsTagsTagResource> createOrFindTagsV1(reachV1ContactsTagsStoreRequest)

Create tags in a profile.  Names that already exist in the profile are not duplicated: the existing tag is returned instead, so the call is safe to repeat. Every tag in the request is returned, whether it was created now or already existed.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration,
    ReachV1ContactsTagsStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ContactsTagsStoreRequest: ReachV1ContactsTagsStoreRequest; //

const { status, data } = await apiInstance.createOrFindTagsV1(
    profileUuid,
    reachV1ContactsTagsStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsTagsStoreRequest** | **ReachV1ContactsTagsStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1ContactsTagsTagResource>**

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

# **deleteATagV1**
> CommonSuccessEmptyResource deleteATagV1()

Delete a tag and remove it from every contact carrying it.  The contacts themselves are not deleted. This is idempotent: deleting a tag that does not exist in the profile still succeeds.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let tagUuid: string; //Tag uuid parameter (default to undefined)

const { status, data } = await apiInstance.deleteATagV1(
    profileUuid,
    tagUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **tagUuid** | [**string**] | Tag uuid parameter | defaults to undefined|


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

# **listProfileTagsV1**
> Array<ReachV1ContactsTagsTagResource> listProfileTagsV1()

Get all tags defined in a profile.  Tags are the way contacts are grouped in Reach, and can be used to filter the contact list or to build segments.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listProfileTagsV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1ContactsTagsTagResource>**

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

# **removeAContactFromATagV1**
> CommonSuccessEmptyResource removeAContactFromATagV1()

Remove a tag from a single contact.  Unlike the bulk endpoint this is applied immediately rather than queued. Neither the tag nor the contact is deleted.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let tagUuid: string; //Tag uuid parameter (default to undefined)
let contactUuid: string; //Contact uuid parameter (default to undefined)

const { status, data } = await apiInstance.removeAContactFromATagV1(
    profileUuid,
    tagUuid,
    contactUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **tagUuid** | [**string**] | Tag uuid parameter | defaults to undefined|
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

# **removeContactsFromATagV1**
> CommonSuccessEmptyResource removeContactsFromATagV1(reachV1ContactsTagsManageContactsRequest)

Remove a tag from many contacts at once.  Pass `contact_uuids` to target specific contacts, or `all_contacts` to target every contact in the profile. The work is queued, so a success response means it was accepted rather than finished. The tag itself and the contacts are not deleted.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration,
    ReachV1ContactsTagsManageContactsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let tagUuid: string; //Tag uuid parameter (default to undefined)
let reachV1ContactsTagsManageContactsRequest: ReachV1ContactsTagsManageContactsRequest; //

const { status, data } = await apiInstance.removeContactsFromATagV1(
    profileUuid,
    tagUuid,
    reachV1ContactsTagsManageContactsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsTagsManageContactsRequest** | **ReachV1ContactsTagsManageContactsRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **tagUuid** | [**string**] | Tag uuid parameter | defaults to undefined|


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

# **renameATagV1**
> ReachV1ContactsTagsTagResource renameATagV1(reachV1ContactsTagsUpdateRequest)

Rename a tag.  The contacts assigned to the tag are unaffected. Names are unique within a profile, so renaming a tag to a name that is already taken is rejected.

### Example

```typescript
import {
    ReachTagsApi,
    Configuration,
    ReachV1ContactsTagsUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachTagsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let tagUuid: string; //Tag uuid parameter (default to undefined)
let reachV1ContactsTagsUpdateRequest: ReachV1ContactsTagsUpdateRequest; //

const { status, data } = await apiInstance.renameATagV1(
    profileUuid,
    tagUuid,
    reachV1ContactsTagsUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsTagsUpdateRequest** | **ReachV1ContactsTagsUpdateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **tagUuid** | [**string**] | Tag uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsTagsTagResource**

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

