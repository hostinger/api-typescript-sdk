# ReachAutomationsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAutomationDetailsV1**](#getautomationdetailsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/automations/{automationUuid} | Get automation details|
|[**listAutomationStepsV1**](#listautomationstepsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/automations/{automationUuid}/steps | List automation steps|
|[**listAutomationsV1**](#listautomationsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/automations | List automations|

# **getAutomationDetailsV1**
> ReachV1AutomationsAutomationResource getAutomationDetailsV1()

Get a single automation with the counts of contacts that entered it, are moving through it, finished it or failed on the way.  This describes the automation itself. To see the workflow it runs, use the steps endpoint.

### Example

```typescript
import {
    ReachAutomationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachAutomationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let automationUuid: string; //Automation uuid parameter (default to undefined)

const { status, data } = await apiInstance.getAutomationDetailsV1(
    profileUuid,
    automationUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **automationUuid** | [**string**] | Automation uuid parameter | defaults to undefined|


### Return type

**ReachV1AutomationsAutomationResource**

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

# **listAutomationStepsV1**
> Array<ReachV1AutomationsStepsAutomationStepResource> listAutomationStepsV1()

Get the workflow of an automation as a flat list of steps.  The steps form a tree rather than a straight line: follow `parent_uuid` to reconstruct the branches, and use `step_order` to order the steps that share a parent. An automation with no steps yet returns an empty list.

### Example

```typescript
import {
    ReachAutomationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachAutomationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let automationUuid: string; //Automation uuid parameter (default to undefined)

const { status, data } = await apiInstance.listAutomationStepsV1(
    profileUuid,
    automationUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **automationUuid** | [**string**] | Automation uuid parameter | defaults to undefined|


### Return type

**Array<ReachV1AutomationsStepsAutomationStepResource>**

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

# **listAutomationsV1**
> ReachListAutomationsV1200Response listAutomationsV1()

Get a paginated list of the automations in a profile.  Every automation comes with the counts of contacts that entered it, are moving through it, finished it or failed on the way. Those counts describe the contact journey and are not email engagement metrics - for opens, clicks and unsubscribes use the campaign statistics endpoint instead.

### Example

```typescript
import {
    ReachAutomationsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachAutomationsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let status: 'active' | 'paused' | 'draft'; //Filter automations by status.  There is no `completed` status. An automation that has finished for every contact still reports `active`. (optional) (default to undefined)
let sortDirection: 'asc' | 'desc'; //Order automations by creation date. Newest first unless set to `asc`. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listAutomationsV1(
    profileUuid,
    status,
    sortDirection,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **status** | [**&#39;active&#39; | &#39;paused&#39; | &#39;draft&#39;**]**Array<&#39;active&#39; &#124; &#39;paused&#39; &#124; &#39;draft&#39;>** | Filter automations by status.  There is no &#x60;completed&#x60; status. An automation that has finished for every contact still reports &#x60;active&#x60;. | (optional) defaults to undefined|
| **sortDirection** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | Order automations by creation date. Newest first unless set to &#x60;asc&#x60;. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**ReachListAutomationsV1200Response**

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

