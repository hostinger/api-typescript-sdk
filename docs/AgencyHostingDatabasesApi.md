# AgencyHostingDatabasesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAgencyPlanWebsiteDatabaseUserV1**](#createagencyplanwebsitedatabaseuserv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/databases/{database_name}/users | Create Agency Plan website database user|
|[**createAgencyPlanWebsiteDatabaseV1**](#createagencyplanwebsitedatabasev1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/databases | Create Agency Plan website database|
|[**deleteAgencyPlanWebsiteDatabaseUserV1**](#deleteagencyplanwebsitedatabaseuserv1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid}/databases/{database_name}/users/{database_user_name} | Delete Agency Plan website database user|
|[**deleteAgencyPlanWebsiteDatabaseV1**](#deleteagencyplanwebsitedatabasev1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid}/databases/{database_name} | Delete Agency Plan website database|
|[**listAgencyPlanWebsiteDatabasesV1**](#listagencyplanwebsitedatabasesv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/databases | List Agency Plan website databases|

# **createAgencyPlanWebsiteDatabaseUserV1**
> AgencyHostingV1WebsitesDatabasesDatabaseUserResource createAgencyPlanWebsiteDatabaseUserV1(agencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest)

Creates a user for an existing database on an Agency Plan website.  Each database supports a single non-system user; creating a user for a database that already has one fails.

### Example

```typescript
import {
    AgencyHostingDatabasesApi,
    Configuration,
    AgencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDatabasesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let databaseName: string; //Full database name as returned by the list databases endpoint. (default to undefined)
let agencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest: AgencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest; //

const { status, data } = await apiInstance.createAgencyPlanWebsiteDatabaseUserV1(
    websiteUid,
    databaseName,
    agencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest** | **AgencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **databaseName** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|


### Return type

**AgencyHostingV1WebsitesDatabasesDatabaseUserResource**

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

# **createAgencyPlanWebsiteDatabaseV1**
> AgencyHostingV1WebsitesDatabasesDatabaseResource createAgencyPlanWebsiteDatabaseV1(agencyHostingV1WebsitesDatabasesCreateDatabaseRequest)

Creates a MySQL database with a dedicated user for an Agency Plan website.  The database name, username, and password must all be provided by the caller.

### Example

```typescript
import {
    AgencyHostingDatabasesApi,
    Configuration,
    AgencyHostingV1WebsitesDatabasesCreateDatabaseRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDatabasesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1WebsitesDatabasesCreateDatabaseRequest: AgencyHostingV1WebsitesDatabasesCreateDatabaseRequest; //

const { status, data } = await apiInstance.createAgencyPlanWebsiteDatabaseV1(
    websiteUid,
    agencyHostingV1WebsitesDatabasesCreateDatabaseRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1WebsitesDatabasesCreateDatabaseRequest** | **AgencyHostingV1WebsitesDatabasesCreateDatabaseRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**AgencyHostingV1WebsitesDatabasesDatabaseResource**

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

# **deleteAgencyPlanWebsiteDatabaseUserV1**
> CommonSuccessEmptyResource deleteAgencyPlanWebsiteDatabaseUserV1()

Permanently deletes a database user from an Agency Plan website database, revoking all access it had.  The operation is idempotent: deleting a user that does not exist succeeds without error.

### Example

```typescript
import {
    AgencyHostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDatabasesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let databaseName: string; //Full database name as returned by the list databases endpoint. (default to undefined)
let databaseUserName: string; //Database username as returned by the list databases endpoint. (default to undefined)

const { status, data } = await apiInstance.deleteAgencyPlanWebsiteDatabaseUserV1(
    websiteUid,
    databaseName,
    databaseUserName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **databaseName** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|
| **databaseUserName** | [**string**] | Database username as returned by the list databases endpoint. | defaults to undefined|


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

# **deleteAgencyPlanWebsiteDatabaseV1**
> CommonSuccessEmptyResource deleteAgencyPlanWebsiteDatabaseV1()

Permanently deletes a MySQL database and all its data from an Agency Plan website, including its users.  The operation is idempotent: deleting a database that does not exist succeeds without error.

### Example

```typescript
import {
    AgencyHostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDatabasesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let databaseName: string; //Full database name as returned by the list databases endpoint. (default to undefined)

const { status, data } = await apiInstance.deleteAgencyPlanWebsiteDatabaseV1(
    websiteUid,
    databaseName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **databaseName** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|


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

# **listAgencyPlanWebsiteDatabasesV1**
> AgencyHostingListAgencyPlanWebsiteDatabasesV1200Response listAgencyPlanWebsiteDatabasesV1()

Returns a paginated list of MySQL databases created for an Agency Plan website.  Each entry includes the database\'s non-system users.

### Example

```typescript
import {
    AgencyHostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDatabasesApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAgencyPlanWebsiteDatabasesV1(
    websiteUid,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**AgencyHostingListAgencyPlanWebsiteDatabasesV1200Response**

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

