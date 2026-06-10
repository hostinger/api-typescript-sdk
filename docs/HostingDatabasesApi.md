# HostingDatabasesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**changeDatabasePasswordV1**](#changedatabasepasswordv1) | **PATCH** /api/hosting/v1/accounts/{username}/databases/{name}/change-password | Change database password|
|[**createAccountDatabaseV1**](#createaccountdatabasev1) | **POST** /api/hosting/v1/accounts/{username}/databases | Create account database|
|[**deleteAccountDatabaseV1**](#deleteaccountdatabasev1) | **DELETE** /api/hosting/v1/accounts/{username}/databases/{name} | Delete account database|
|[**getPhpMyAdminLinkV1**](#getphpmyadminlinkv1) | **GET** /api/hosting/v1/accounts/{username}/databases/{name}/phpmyadmin-link | Get phpMyAdmin link|
|[**listAccountDatabasesV1**](#listaccountdatabasesv1) | **GET** /api/hosting/v1/accounts/{username}/databases | List account databases|
|[**repairDatabaseV1**](#repairdatabasev1) | **PATCH** /api/hosting/v1/accounts/{username}/databases/{name}/repair | Repair database|

# **changeDatabasePasswordV1**
> CommonSuccessEmptyResource changeDatabasePasswordV1(hostingV1DatabasesChangeDatabasePasswordRequest)

Changes the password for the specified database user.  The database name must be the full name returned by the list databases endpoint. The password must also be updated in any website configuration that uses this database.

### Example

```typescript
import {
    HostingDatabasesApi,
    Configuration,
    HostingV1DatabasesChangeDatabasePasswordRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatabasesApi(configuration);

let username: string; // (default to undefined)
let name: string; //Full database name as returned by the list databases endpoint. (default to undefined)
let hostingV1DatabasesChangeDatabasePasswordRequest: HostingV1DatabasesChangeDatabasePasswordRequest; //

const { status, data } = await apiInstance.changeDatabasePasswordV1(
    username,
    name,
    hostingV1DatabasesChangeDatabasePasswordRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1DatabasesChangeDatabasePasswordRequest** | **HostingV1DatabasesChangeDatabasePasswordRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **name** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|


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

# **createAccountDatabaseV1**
> CommonSuccessEmptyResource createAccountDatabaseV1(hostingV1DatabasesCreateDatabaseRequest)

Creates a database with a database user and password for the specified account.  The database name and user are automatically prefixed with the account username when needed.

### Example

```typescript
import {
    HostingDatabasesApi,
    Configuration,
    HostingV1DatabasesCreateDatabaseRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatabasesApi(configuration);

let username: string; // (default to undefined)
let hostingV1DatabasesCreateDatabaseRequest: HostingV1DatabasesCreateDatabaseRequest; //

const { status, data } = await apiInstance.createAccountDatabaseV1(
    username,
    hostingV1DatabasesCreateDatabaseRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1DatabasesCreateDatabaseRequest** | **HostingV1DatabasesCreateDatabaseRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|


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

# **deleteAccountDatabaseV1**
> CommonSuccessEmptyResource deleteAccountDatabaseV1()

Permanently deletes a database and its remote connections.  The database name must be the full name returned by the list databases endpoint.

### Example

```typescript
import {
    HostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatabasesApi(configuration);

let username: string; // (default to undefined)
let name: string; //Full database name as returned by the list databases endpoint. (default to undefined)

const { status, data } = await apiInstance.deleteAccountDatabaseV1(
    username,
    name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **name** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|


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

# **getPhpMyAdminLinkV1**
> HostingV1DatabasesPhpMyAdminLinkResource getPhpMyAdminLinkV1()

Returns a direct sign-on link to phpMyAdmin for the specified database.  Use this when a visual database interface is needed for SQL queries, imports, exports, or table management. The database name must be the full name returned by the list databases endpoint.

### Example

```typescript
import {
    HostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatabasesApi(configuration);

let username: string; // (default to undefined)
let name: string; //Full database name as returned by the list databases endpoint. (default to undefined)

const { status, data } = await apiInstance.getPhpMyAdminLinkV1(
    username,
    name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **name** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|


### Return type

**HostingV1DatabasesPhpMyAdminLinkResource**

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

# **listAccountDatabasesV1**
> HostingListAccountDatabasesV1200Response listAccountDatabasesV1()

Returns a paginated list of databases for the specified account.  Use the domain and is_assigned filters to find databases assigned to a specific domain.

### Example

```typescript
import {
    HostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatabasesApi(configuration);

let username: string; // (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let domain: string; //Filter by domain name (exact match) (optional) (default to undefined)
let isAssigned: boolean; //When used with domain, return only databases assigned to that domain. (optional) (default to undefined)
let search: string; //Search databases by name, user, or creation date. (optional) (default to undefined)

const { status, data } = await apiInstance.listAccountDatabasesV1(
    username,
    page,
    perPage,
    domain,
    isAssigned,
    search
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **domain** | [**string**] | Filter by domain name (exact match) | (optional) defaults to undefined|
| **isAssigned** | [**boolean**] | When used with domain, return only databases assigned to that domain. | (optional) defaults to undefined|
| **search** | [**string**] | Search databases by name, user, or creation date. | (optional) defaults to undefined|


### Return type

**HostingListAccountDatabasesV1200Response**

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

# **repairDatabaseV1**
> CommonSuccessEmptyResource repairDatabaseV1()

Repairs corrupted database tables asynchronously.  Use when database errors, crashes, or corruption are reported. The database name must be the full name returned by the list databases endpoint.

### Example

```typescript
import {
    HostingDatabasesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingDatabasesApi(configuration);

let username: string; // (default to undefined)
let name: string; //Full database name as returned by the list databases endpoint. (default to undefined)

const { status, data } = await apiInstance.repairDatabaseV1(
    username,
    name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **name** | [**string**] | Full database name as returned by the list databases endpoint. | defaults to undefined|


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

