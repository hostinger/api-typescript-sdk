# HostingCronJobsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAccountCronJobV1**](#createaccountcronjobv1) | **POST** /api/hosting/v1/accounts/{username}/cron-jobs | Create account cron job|
|[**deleteAccountCronJobV1**](#deleteaccountcronjobv1) | **DELETE** /api/hosting/v1/accounts/{username}/cron-jobs/{uid} | Delete account cron job|
|[**getCronJobOutputV1**](#getcronjoboutputv1) | **GET** /api/hosting/v1/accounts/{username}/cron-jobs/{uid}/output | Get cron job output|
|[**listAccountCronJobsV1**](#listaccountcronjobsv1) | **GET** /api/hosting/v1/accounts/{username}/cron-jobs | List account cron jobs|

# **createAccountCronJobV1**
> HostingV1CronJobsCronJobResource createAccountCronJobV1(hostingV1CronJobsCreateCronJobRequest)

Creates a cron job for the specified account from a schedule expression and a command.  Returns the created cron job, including its uid, which is required to delete the cron job or fetch its output.

### Example

```typescript
import {
    HostingCronJobsApi,
    Configuration,
    HostingV1CronJobsCreateCronJobRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCronJobsApi(configuration);

let username: string; // (default to undefined)
let hostingV1CronJobsCreateCronJobRequest: HostingV1CronJobsCreateCronJobRequest; //

const { status, data } = await apiInstance.createAccountCronJobV1(
    username,
    hostingV1CronJobsCreateCronJobRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1CronJobsCreateCronJobRequest** | **HostingV1CronJobsCreateCronJobRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|


### Return type

**HostingV1CronJobsCronJobResource**

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

# **deleteAccountCronJobV1**
> CommonSuccessEmptyResource deleteAccountCronJobV1()

Permanently deletes the cron job identified by its uid.  The uid is returned by the list cron jobs endpoint.

### Example

```typescript
import {
    HostingCronJobsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCronJobsApi(configuration);

let username: string; // (default to undefined)
let uid: string; //Unique identifier of the cron job as returned by the list cron jobs endpoint. (default to undefined)

const { status, data } = await apiInstance.deleteAccountCronJobV1(
    username,
    uid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **uid** | [**string**] | Unique identifier of the cron job as returned by the list cron jobs endpoint. | defaults to undefined|


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

# **getCronJobOutputV1**
> HostingV1CronJobsCronJobOutputResource getCronJobOutputV1()

Returns the output captured from the last execution of the cron job identified by its uid.  The uid is returned by the list cron jobs endpoint.

### Example

```typescript
import {
    HostingCronJobsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCronJobsApi(configuration);

let username: string; // (default to undefined)
let uid: string; //Unique identifier of the cron job as returned by the list cron jobs endpoint. (default to undefined)

const { status, data } = await apiInstance.getCronJobOutputV1(
    username,
    uid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **uid** | [**string**] | Unique identifier of the cron job as returned by the list cron jobs endpoint. | defaults to undefined|


### Return type

**HostingV1CronJobsCronJobOutputResource**

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

# **listAccountCronJobsV1**
> Array<HostingV1CronJobsCronJobResource> listAccountCronJobsV1()

Returns the list of cron jobs configured for the specified account, including their schedule and command.

### Example

```typescript
import {
    HostingCronJobsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingCronJobsApi(configuration);

let username: string; // (default to undefined)

const { status, data } = await apiInstance.listAccountCronJobsV1(
    username
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|


### Return type

**Array<HostingV1CronJobsCronJobResource>**

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

