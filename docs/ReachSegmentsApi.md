# ReachSegmentsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createANewContactSegmentV1**](#createanewcontactsegmentv1) | **POST** /api/reach/v1/segmentation/segments | Create a new contact segment|
|[**getSegmentDetailsV1**](#getsegmentdetailsv1) | **GET** /api/reach/v1/segmentation/segments/{segmentUuid} | Get segment details|
|[**listProfileSegmentContactsV1**](#listprofilesegmentcontactsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/segmentation/segments/{segmentUuid}/contacts | List profile segment contacts|
|[**listSegmentContactsV1**](#listsegmentcontactsv1) | **GET** /api/reach/v1/segmentation/segments/{segmentUuid}/contacts | List segment contacts|
|[**listSegmentsV1**](#listsegmentsv1) | **GET** /api/reach/v1/segmentation/segments | List segments|

# **createANewContactSegmentV1**
> ReachV1ContactsSegmentsSegmentResource createANewContactSegmentV1(reachV1ContactsSegmentsStoreRequest)

Create a new contact segment.  This endpoint allows creating a new contact segment that can be used to organize contacts. The segment can be configured with specific criteria like email, name, subscription status, etc.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration,
    ReachV1ContactsSegmentsStoreRequest
} from 'hostinger-api-sdk';

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

# **getSegmentDetailsV1**
> ReachV1ContactsSegmentsSegmentResource getSegmentDetailsV1()

Get details of a specific segment.  This endpoint retrieves information about a single segment identified by UUID. Segments are used to organize and group contacts based on specific criteria.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from 'hostinger-api-sdk';

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
} from 'hostinger-api-sdk';

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

# **listSegmentContactsV1**
> ReachListProfileSegmentContactsV1200Response listSegmentContactsV1()

Retrieve contacts associated with a specific segment.  This endpoint allows you to fetch and filter contacts that belong to a particular segment, identified by its UUID.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from 'hostinger-api-sdk';

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

# **listSegmentsV1**
> Array<ReachV1ContactsSegmentsContactSegmentResource> listSegmentsV1()

Get a list of all contact segments.  This endpoint returns a list of contact segments that can be used to organize contacts.

### Example

```typescript
import {
    ReachSegmentsApi,
    Configuration
} from 'hostinger-api-sdk';

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

