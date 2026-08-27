# ReachSegmentsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**countProfileSegmentContactsV1**](#countprofilesegmentcontactsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid}/count | Count profile segment contacts|
|[**createANewContactSegmentV1**](#createanewcontactsegmentv1) | **POST** /api/reach/v1/segmentation/segments | Create a new contact segment|
|[**createAProfileSegmentV1**](#createaprofilesegmentv1) | **POST** /api/reach/v1/profiles/{profileUuid}/segmentation/segments | Create a profile segment|
|[**deleteAProfileSegmentV1**](#deleteaprofilesegmentv1) | **DELETE** /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid} | Delete a profile segment|
|[**getProfileSegmentDetailsV1**](#getprofilesegmentdetailsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid} | Get profile segment details|
|[**getSegmentDetailsV1**](#getsegmentdetailsv1) | **GET** /api/reach/v1/segmentation/segments/{segmentUuid} | Get segment details|
|[**listProfileSegmentContactsV1**](#listprofilesegmentcontactsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid}/contacts | List profile segment contacts|
|[**listProfileSegmentsV1**](#listprofilesegmentsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/segmentation/segments | List profile segments|
|[**listSegmentContactsV1**](#listsegmentcontactsv1) | **GET** /api/reach/v1/segmentation/segments/{segmentUuid}/contacts | List segment contacts|
|[**listSegmentFilterAttributesV1**](#listsegmentfilterattributesv1) | **GET** /api/reach/v1/profiles/{profileUuid}/segmentation/filters/attributes | List segment filter attributes|
|[**listSegmentsV1**](#listsegmentsv1) | **GET** /api/reach/v1/segmentation/segments | List segments|
|[**previewContactsMatchingConditionsV1**](#previewcontactsmatchingconditionsv1) | **POST** /api/reach/v1/profiles/{profileUuid}/segmentation/filters/contacts | Preview contacts matching conditions|
|[**updateAProfileSegmentV1**](#updateaprofilesegmentv1) | **PUT** /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid} | Update a profile segment|

# **countProfileSegmentContactsV1**
> ReachV1ContactsSegmentsSegmentContactsCountResource countProfileSegmentContactsV1()

Count the contacts currently matching a segment without listing them.  Cheaper than paging through the segment contacts endpoint when only the size is needed.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let segmentUuid: string; //Segment uuid parameter (default to undefined)

const { status, data } = await apiInstance.countProfileSegmentContactsV1(
    profileUuid,
    segmentUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsSegmentsSegmentContactsCountResource**

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

# **createANewContactSegmentV1**
> ReachV1ContactsSegmentsSegmentResource createANewContactSegmentV1(reachV1ContactsSegmentsStoreRequest)

Create a new contact segment.  This endpoint allows creating a new contact segment that can be used to organize contacts. The segment can be configured with specific criteria like email, name, subscription status, etc.  **Deprecated.** This endpoint cannot target a profile, so it always falls back to the client\'s default profile and cannot create segments in any other profile. Use `POST /api/reach/v1/profiles/{profileUuid}/segmentation/segments` instead.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration,
    ReachV1ContactsSegmentsStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let reachV1ContactsSegmentsStoreRequest: ReachV1ContactsSegmentsStoreRequest; //

const { status, data } = await apiInstance.createANewContactSegmentV1(
    reachV1ContactsSegmentsStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsSegmentsStoreRequest** | **ReachV1ContactsSegmentsStoreRequest**|  | |


### Return type

**ReachV1ContactsSegmentsSegmentResource**

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

# **createAProfileSegmentV1**
> ReachV1ContactsSegmentsSegmentResource createAProfileSegmentV1(reachV1ContactsSegmentsProfileStoreRequest)

Create a segment in a profile.  A segment is a saved set of conditions rather than a fixed list, so its membership changes as contacts change. Creating one does not modify any contact.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration,
    ReachV1ContactsSegmentsProfileStoreRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ContactsSegmentsProfileStoreRequest: ReachV1ContactsSegmentsProfileStoreRequest; //

const { status, data } = await apiInstance.createAProfileSegmentV1(
    profileUuid,
    reachV1ContactsSegmentsProfileStoreRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsSegmentsProfileStoreRequest** | **ReachV1ContactsSegmentsProfileStoreRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsSegmentsSegmentResource**

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

# **deleteAProfileSegmentV1**
> CommonSuccessEmptyResource deleteAProfileSegmentV1()

Delete a segment.  Only the segment definition is removed. The contacts that matched it are left untouched.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let segmentUuid: string; //Segment uuid parameter (default to undefined)

const { status, data } = await apiInstance.deleteAProfileSegmentV1(
    profileUuid,
    segmentUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|


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

# **getProfileSegmentDetailsV1**
> ReachV1ContactsSegmentsSegmentResource getProfileSegmentDetailsV1()

Get a single segment of a profile, including the conditions that define it.  To retrieve the contacts currently matching those conditions, use the segment contacts endpoint instead.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let segmentUuid: string; //Segment uuid parameter (default to undefined)

const { status, data } = await apiInstance.getProfileSegmentDetailsV1(
    profileUuid,
    segmentUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsSegmentsSegmentResource**

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

# **getSegmentDetailsV1**
> ReachV1ContactsSegmentsSegmentResource getSegmentDetailsV1()

Get details of a specific segment.  This endpoint retrieves information about a single segment identified by UUID. Segments are used to organize and group contacts based on specific criteria.  **Deprecated.** This endpoint cannot target a profile, so it always falls back to the client\'s default profile and cannot read segments of any other profile. Use `GET /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid}` instead.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let segmentUuid: string; //Segment uuid parameter (default to undefined)

const { status, data } = await apiInstance.getSegmentDetailsV1(
    segmentUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsSegmentsSegmentResource**

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

# **listProfileSegmentContactsV1**
> ReachListProfileSegmentContactsV1200Response listProfileSegmentContactsV1()

Retrieve contacts associated with a specific segment for a given profile.  This endpoint allows you to fetch and filter contacts that belong to a particular segment, identified by its UUID, scoped to a specific profile.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let segmentUuid: string; //Segment uuid parameter (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listProfileSegmentContactsV1(
    profileUuid,
    segmentUuid,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**ReachListProfileSegmentContactsV1200Response**

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

# **listProfileSegmentsV1**
> ReachListProfileSegmentsV1200Response listProfileSegmentsV1()

Get a paginated list of the segments defined in a profile.  Each entry carries the number of contacts currently matching it, which is recalculated on read rather than stored. Use `count_type` to count either every matching contact or only the subscribed ones.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let countType: 'all' | 'subscribed'; //Which matching contacts to count for each segment (optional) (default to 'all')
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listProfileSegmentsV1(
    profileUuid,
    countType,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **countType** | [**&#39;all&#39; | &#39;subscribed&#39;**]**Array<&#39;all&#39; &#124; &#39;subscribed&#39;>** | Which matching contacts to count for each segment | (optional) defaults to 'all'|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**ReachListProfileSegmentsV1200Response**

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

# **listSegmentContactsV1**
> ReachListProfileSegmentContactsV1200Response listSegmentContactsV1()

Retrieve contacts associated with a specific segment.  This endpoint allows you to fetch and filter contacts that belong to a particular segment, identified by its UUID.  **Deprecated.** This endpoint cannot target a profile, so it always falls back to the client\'s default profile and cannot read segments of any other profile. Use `GET /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid}/contacts` instead.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let segmentUuid: string; //Segment uuid parameter (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listSegmentContactsV1(
    segmentUuid,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**ReachListProfileSegmentContactsV1200Response**

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

# **listSegmentFilterAttributesV1**
> ReachV1ContactsSegmentsSegmentFilterAttributesResource listSegmentFilterAttributesV1()

List every attribute a segment condition can filter on, with the operators each attribute accepts, the value format they expect and, where the value is constrained, the allowed values.  The list is profile specific: it includes the profile\'s custom contact fields, its tags and its 20 most recently published campaigns, so the valid attributes cannot be hardcoded. Read it before creating or updating a segment to discover the valid `attribute`, `operator` and `value` combinations.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)

const { status, data } = await apiInstance.listSegmentFilterAttributesV1(
    profileUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsSegmentsSegmentFilterAttributesResource**

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

# **listSegmentsV1**
> Array<ReachV1ContactsSegmentsContactSegmentResource> listSegmentsV1()

Get a list of all contact segments.  This endpoint returns a list of contact segments that can be used to organize contacts.  **Deprecated.** This endpoint cannot target a profile, so it always falls back to the client\'s default profile and cannot list the segments of any other profile. Use `GET /api/reach/v1/profiles/{profileUuid}/segmentation/segments` instead.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

const { status, data } = await apiInstance.listSegmentsV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<ReachV1ContactsSegmentsContactSegmentResource>**

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

# **previewContactsMatchingConditionsV1**
> ReachListProfileContactsV1200Response previewContactsMatchingConditionsV1(reachV1ContactsSegmentsProfileFilterContactsRequest)

Preview the contacts matching a set of conditions without saving a segment.  The body is the same set of conditions accepted when creating or updating a segment, so this is how to check who a filter reaches, and how many, before persisting it. Nothing is stored and no contact is modified.  Call the segment filter attributes endpoint first to discover the valid `attribute`, `operator` and `value` combinations.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration,
    ReachV1ContactsSegmentsProfileFilterContactsRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let reachV1ContactsSegmentsProfileFilterContactsRequest: ReachV1ContactsSegmentsProfileFilterContactsRequest; //

const { status, data } = await apiInstance.previewContactsMatchingConditionsV1(
    profileUuid,
    reachV1ContactsSegmentsProfileFilterContactsRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsSegmentsProfileFilterContactsRequest** | **ReachV1ContactsSegmentsProfileFilterContactsRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|


### Return type

**ReachListProfileContactsV1200Response**

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

# **updateAProfileSegmentV1**
> ReachV1ContactsSegmentsSegmentResource updateAProfileSegmentV1(reachV1ContactsSegmentsProfileUpdateRequest)

Rename a segment and/or replace the conditions that define it.  `name` is always required. Omit `conditions` to rename without touching the conditions; supply them and they replace the existing set entirely rather than being merged into it. Contacts are never modified, but which of them match the segment can change immediately.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration,
    ReachV1ContactsSegmentsProfileUpdateRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new ReachSegmentsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let segmentUuid: string; //Segment uuid parameter (default to undefined)
let reachV1ContactsSegmentsProfileUpdateRequest: ReachV1ContactsSegmentsProfileUpdateRequest; //

const { status, data } = await apiInstance.updateAProfileSegmentV1(
    profileUuid,
    segmentUuid,
    reachV1ContactsSegmentsProfileUpdateRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **reachV1ContactsSegmentsProfileUpdateRequest** | **ReachV1ContactsSegmentsProfileUpdateRequest**|  | |
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **segmentUuid** | [**string**] | Segment uuid parameter | defaults to undefined|


### Return type

**ReachV1ContactsSegmentsSegmentResource**

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

