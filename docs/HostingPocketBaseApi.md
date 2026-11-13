# HostingPocketBaseApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createPocketBaseBackendV1**](#createpocketbasebackendv1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/pocketbase | Create PocketBase backend|
|[**deletePocketBaseBackendV1**](#deletepocketbasebackendv1) | **DELETE** /api/hosting/v1/accounts/{username}/websites/{domain}/pocketbase | Delete PocketBase backend|
|[**getPocketBaseBackendV1**](#getpocketbasebackendv1) | **GET** /api/hosting/v1/accounts/{username}/websites/{domain}/pocketbase | Get PocketBase backend|
|[**listAccountPocketBaseBackendsV1**](#listaccountpocketbasebackendsv1) | **GET** /api/hosting/v1/accounts/{username}/pocketbase | List account PocketBase backends|
|[**setPocketBaseSuperuserV1**](#setpocketbasesuperuserv1) | **PUT** /api/hosting/v1/accounts/{username}/websites/{domain}/pocketbase/superuser | Set PocketBase superuser|

# **createPocketBaseBackendV1**
> HostingV1PocketBaseBackendCreatedResource createPocketBaseBackendV1()

Creates a PocketBase backend for a website: a database, authentication, file storage and a realtime REST API, served from the website\'s own domain. A website has at most one PocketBase backend. Creation usually takes a few seconds.  The backend takes over the `/api` and `/_` paths of the website: from then on requests to these paths and everything below them go to PocketBase, while every other path keeps serving the website. Do not create a backend for a website that serves its own `/api` or `/_` paths, because they stop working; confirm with the user before calling it. Deleting the backend gives both paths back to the website. Headless WordPress websites and parked domains are not supported; for a parked domain, use the website it is parked on. A website that already has a backend is rejected with 422, unless that backend is in state `missing`: then it is replaced with a new, empty one. A website set up with `type: headless_empty` becomes `headless_pocketbase`; any other website keeps its type.  `superuser_password` is optional: leave it out to get a strong generated password, or send your own (10-128 characters). The response returns it in `superuser_password` once and Hostinger never stores it, so save it in your app secrets right away; you need it to manage the backend through the PocketBase REST API. If it is lost, set a new one with the `Set PocketBase superuser` endpoint. `superuser_email` defaults to the email of the website owner.  The instance sleeps when idle and wakes on the first request, so the first call after a quiet period can take a few seconds. `next_steps` in the response lists what to do next.  PocketBase is rolling out gradually: an account without access yet gets 422.

### Example

```typescript
import {
    HostingPocketBaseApi,
    Configuration,
    HostingV1PocketBaseCreateBackendRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingPocketBaseApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1PocketBaseCreateBackendRequest: HostingV1PocketBaseCreateBackendRequest; // (optional)

const { status, data } = await apiInstance.createPocketBaseBackendV1(
    username,
    domain,
    hostingV1PocketBaseCreateBackendRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1PocketBaseCreateBackendRequest** | **HostingV1PocketBaseCreateBackendRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1PocketBaseBackendCreatedResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Created response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**429** | Error response |  -  |
|**503** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deletePocketBaseBackendV1**
> CommonSuccessEmptyResource deletePocketBaseBackendV1()

Permanently deletes the PocketBase backend of a website with all its data (collections, records, users and uploaded files) and gives the `/api` and `/_` paths back to the website; a `headless_pocketbase` website becomes `headless_empty`. This cannot be undone and every app using this backend stops working, so confirm with the user before calling it and export the data you need from the dashboard (`admin_url`) first.  Returns success also when the website has no PocketBase backend; then it only clears a `headless_pocketbase` mark. To regain access after losing the superuser password, use the `Set PocketBase superuser` endpoint instead of deleting the backend.  PocketBase is rolling out gradually: an account without access yet gets 422; an unknown website gets 404.

### Example

```typescript
import {
    HostingPocketBaseApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingPocketBaseApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.deletePocketBaseBackendV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**503** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getPocketBaseBackendV1**
> HostingV1PocketBaseBackendResource getPocketBaseBackendV1()

Returns the PocketBase backend of a website: its REST API and dashboard URLs, live state and version. A PocketBase backend gives the website a database, authentication, file storage and a realtime REST API, served from the website\'s own domain under `/api` and `/_`. Returns 404 when the website has no PocketBase backend.  The superuser password is only shown once, when it is set, and is never returned here. If it is lost, set a new one with the `Set PocketBase superuser` endpoint.  The instance sleeps when idle and wakes on the first request, so `asleep` is a normal state and the first call to a sleeping instance can take a few seconds. `starting`, `running` and `stopping` are healthy.  `failed` means the last start did not succeed. Hostinger starts it again on its own after `retry_after_seconds`, and the data is intact: wait and call again, do not delete the backend. `failure_reason` says why: `process_limit` means the hosting account has no free process slots, usually because its Node.js apps are running.  `unregistered` means the instance is broken. `missing` means its files are gone from the server, and creating the PocketBase backend again sets up a new, empty one. `state` is null when the server could not be reached; retry later.  PocketBase is rolling out gradually: an account without access yet gets 422.

### Example

```typescript
import {
    HostingPocketBaseApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingPocketBaseApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.getPocketBaseBackendV1(
    username,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1PocketBaseBackendResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listAccountPocketBaseBackendsV1**
> Array<HostingV1PocketBaseInstanceResource> listAccountPocketBaseBackendsV1()

Lists the PocketBase backends of all websites of a hosting account with their URLs, live state, version and disk usage. A PocketBase backend gives a website a database, authentication, file storage and a realtime REST API, served from the website\'s own domain. An empty list means no website of the account has a PocketBase backend.  States: `asleep` is normal (the instance sleeps when idle and wakes on the first request); `starting`, `running` and `stopping` are healthy.  `failed` means the last start did not succeed. Hostinger starts it again on its own after `retry_after_seconds`, and the data is intact: wait and call again, do not delete the backend. `failure_reason` says why: `process_limit` means the hosting account has no free process slots, usually because its Node.js apps are running.  `unregistered` means the instance is broken. `missing` means its files are gone from the server, and creating the PocketBase backend again sets up a new, empty one. `state` is null when the server could not be reached; retry later.  PocketBase is rolling out gradually: an account without access yet gets 422.

### Example

```typescript
import {
    HostingPocketBaseApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingPocketBaseApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.listAccountPocketBaseBackendsV1(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**Array<HostingV1PocketBaseInstanceResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**404** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **setPocketBaseSuperuserV1**
> HostingV1PocketBaseSuperuserResource setPocketBaseSuperuserV1()

Sets the password of a superuser of the website\'s PocketBase backend, and creates that superuser when there is none with the given email. The old password of that superuser stops working at once, so apps and scripts still using it lose superuser access; confirm with the user before calling it.  Use it when the superuser password is lost (Hostinger never stores it), when it leaked and must be rotated, or to add another superuser with a different email. Returns 404 when the website has no PocketBase backend; create one first. App user accounts are managed through the PocketBase REST API, not here.  `superuser_password` is optional: leave it out to get a strong generated password, or send your own (10-128 characters). The response returns it in `superuser_password` once and Hostinger never stores it, so save it in your app secrets right away, then authenticate again with `pb.collection(\'_superusers\').authWithPassword`. `superuser_email` defaults to the email of the website owner.  PocketBase is rolling out gradually: an account without access yet gets 422.

### Example

```typescript
import {
    HostingPocketBaseApi,
    Configuration,
    HostingV1PocketBaseUpdateSuperuserRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingPocketBaseApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1PocketBaseUpdateSuperuserRequest: HostingV1PocketBaseUpdateSuperuserRequest; // (optional)

const { status, data } = await apiInstance.setPocketBaseSuperuserV1(
    username,
    domain,
    hostingV1PocketBaseUpdateSuperuserRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1PocketBaseUpdateSuperuserRequest** | **HostingV1PocketBaseUpdateSuperuserRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


### Return type

**HostingV1PocketBaseSuperuserResource**

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
|**404** | Error response |  -  |
|**429** | Error response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

