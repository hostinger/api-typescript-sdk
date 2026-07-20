# AgencyHostingCronJobsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createAgencyPlanWebsiteCronJobV1**](#createagencyplanwebsitecronjobv1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/cron-jobs | Create Agency Plan website cron job|
|[**deleteAgencyPlanWebsiteCronJobV1**](#deleteagencyplanwebsitecronjobv1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid}/cron-jobs/{uuid} | Delete Agency Plan website cron job|
|[**listAgencyPlanWebsiteCronJobsV1**](#listagencyplanwebsitecronjobsv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/cron-jobs | List Agency Plan website cron jobs|

# **createAgencyPlanWebsiteCronJobV1**
> AgencyHostingV1WebsitesCronJobsCronJobResource createAgencyPlanWebsiteCronJobV1(agencyHostingV1WebsitesCronJobsCreateCronJobRequest)

Creates a cron job for an Agency Plan website from a schedule expression and a command.  Returns the created cron job, including its uuid, which is required to delete the cron job.

### Example

```typescript
import {
    AgencyHostingCronJobsApi,
    Configuration,
    AgencyHostingV1WebsitesCronJobsCreateCronJobRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingCronJobsApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1WebsitesCronJobsCreateCronJobRequest: AgencyHostingV1WebsitesCronJobsCreateCronJobRequest; //

const { status, data } = await apiInstance.createAgencyPlanWebsiteCronJobV1(
    websiteUid,
    agencyHostingV1WebsitesCronJobsCreateCronJobRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1WebsitesCronJobsCreateCronJobRequest** | **AgencyHostingV1WebsitesCronJobsCreateCronJobRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**AgencyHostingV1WebsitesCronJobsCronJobResource**

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

# **deleteAgencyPlanWebsiteCronJobV1**
> CommonSuccessEmptyResource deleteAgencyPlanWebsiteCronJobV1()

Permanently deletes the cron job identified by its uuid from an Agency Plan website.  The operation is idempotent: deleting a cron job that does not exist succeeds without error.

### Example

```typescript
import {
    AgencyHostingCronJobsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingCronJobsApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let uuid: string; //Unique identifier of the cron job as returned by the list cron jobs endpoint. (default to undefined)

const { status, data } = await apiInstance.deleteAgencyPlanWebsiteCronJobV1(
    websiteUid,
    uuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **uuid** | [**string**] | Unique identifier of the cron job as returned by the list cron jobs endpoint. | defaults to undefined|


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

# **listAgencyPlanWebsiteCronJobsV1**
> AgencyHostingListAgencyPlanWebsiteCronJobsV1200Response listAgencyPlanWebsiteCronJobsV1()

Returns a paginated list of cron jobs configured for an Agency Plan website.  Each entry includes the schedule expression and the command executed on that schedule.

### Example

```typescript
import {
    AgencyHostingCronJobsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingCronJobsApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAgencyPlanWebsiteCronJobsV1(
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

**AgencyHostingListAgencyPlanWebsiteCronJobsV1200Response**

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

