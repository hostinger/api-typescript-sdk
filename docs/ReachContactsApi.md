# ReachContactsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createANewContactV1**](#createanewcontactv1) | **POST** /api/reach/v1/contacts | Create a new contact|
|[**deleteAContactV1**](#deleteacontactv1) | **DELETE** /api/reach/v1/contacts/{uuid} | Delete a contact|
|[**listContactGroupsV1**](#listcontactgroupsv1) | **GET** /api/reach/v1/contacts/groups | List contact groups|
|[**listContactsV1**](#listcontactsv1) | **GET** /api/reach/v1/contacts | List contacts|

# **createANewContactV1**
> ReachV1ContactsContactResource createANewContactV1(reachV1ContactsStoreRequest)

Create a new contact in the email marketing system.  This endpoint allows you to create a new contact with basic information like name, email, and surname. You can optionally assign the contact to specific groups and add notes.  The contact will be automatically subscribed to email communications.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration,
    ReachV1ContactsStoreRequest
} from 'hostinger-api-sdk';

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

**ReachV1ContactsContactResource**

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

# **deleteAContactV1**
> CommonSuccessEmptyResource deleteAContactV1()

Delete a contact with the specified UUID.  This endpoint permanently removes a contact from the email marketing system.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from 'hostinger-api-sdk';

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

# **listContactGroupsV1**
> Array<ReachV1ContactsGroupsContactGroupResource> listContactGroupsV1()

Get a list of all contact groups.  This endpoint returns a list of contact groups that can be used to organize contacts.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from 'hostinger-api-sdk';

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

Get a list of contacts, optionally filtered by group and subscription status.  This endpoint returns a paginated list of contacts with their basic information. You can filter contacts by group UUID and subscription status.

### Example

```typescript
import {
    ReachContactsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachContactsApi(configuration);

let groupUuid: string; //Filter contacts by group UUID (optional) (default to undefined)
let subscriptionStatus: 'subscribed' | 'unsubscribed'; //Filter contacts by subscription status (optional) (default to undefined)
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
| **subscriptionStatus** | [**&#39;subscribed&#39; | &#39;unsubscribed&#39;**]**Array<&#39;subscribed&#39; &#124; &#39;unsubscribed&#39;>** | Filter contacts by subscription status | (optional) defaults to undefined|
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

