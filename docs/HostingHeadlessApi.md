# HostingHeadlessApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**submitHeadlessBuildReportV1**](#submitheadlessbuildreportv1) | **POST** /api/hosting/v1/headless/agent-reports | Submit headless build report|

# **submitHeadlessBuildReportV1**
> HostingV1HeadlessAgentReportResource submitHeadlessBuildReportV1(hostingV1HeadlessStoreAgentReportRequest)

Submits the build report the headless skill writes at the end of a run (including early stops), so Hostinger can learn where builds get stuck. Send one report per call, with the report JSON as the request body, unchanged. Only send a report when the user agreed to it.  The report must match report.schema.json v1; an invalid report returns 422 and is not stored. The report is linked to the authenticated account, so do not add account details to it.

### Example

```typescript
import {
    HostingHeadlessApi,
    Configuration,
    HostingV1HeadlessStoreAgentReportRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new HostingHeadlessApi(configuration);

let hostingV1HeadlessStoreAgentReportRequest: HostingV1HeadlessStoreAgentReportRequest; //

const { status, data } = await apiInstance.submitHeadlessBuildReportV1(
    hostingV1HeadlessStoreAgentReportRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1HeadlessStoreAgentReportRequest** | **HostingV1HeadlessStoreAgentReportRequest**|  | |


### Return type

**HostingV1HeadlessAgentReportResource**

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
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

