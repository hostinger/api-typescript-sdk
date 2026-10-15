# AgentReadinessScansApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAgentReadinessScanV1**](#getagentreadinessscanv1) | **GET** /api/agent-readiness/v1/scans/{domain} | Get agent readiness scan|
|[**runAgentReadinessScanV1**](#runagentreadinessscanv1) | **POST** /api/agent-readiness/v1/scans | Run agent readiness scan|

# **getAgentReadinessScanV1**
> AgentReadinessV1ScansScanResource getAgentReadinessScanV1()

Get the latest agent readiness scan of a website.\\n Scans started with the `Run agent readiness scan` operation are asynchronous. While the status is `pending`, the result fields are null; wait a few seconds and call this operation again until the status is `completed` or `failed`. A `failed` scan is not retried; run the scan again.\\n A completed scan has a 0-100 score, a letter grade, a score per category, and the result of every check with the evidence found and how to fix it. Check names are listed by the `List checks` operation.\\n Returns 404 when the domain has never been scanned; use the `Run agent readiness scan` operation first.

### Example

```typescript
import {
    AgentReadinessScansApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgentReadinessScansApi(configuration);

let domain: string; //Domain name the scan was run for (default to undefined)

const { status, data } = await apiInstance.getAgentReadinessScanV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name the scan was run for | defaults to undefined|


### Return type

**AgentReadinessV1ScansScanResource**

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

# **runAgentReadinessScanV1**
> AgentReadinessV1ScansScanResource runAgentReadinessScanV1(agentReadinessV1ScansRunScanRequest)

Start a scan of how ready a public website is for AI agents to discover, read and act on.\\n Scanning is asynchronous: this operation only starts the scan, and the returned scan is usually `pending` with no results yet. To get the results, poll the `Get agent readiness scan` operation with the same domain every few seconds until its status is `completed` or `failed`. The scan itself is limited to 60 seconds, plus any time it waits in the queue. A `failed` scan is not retried; run this operation again.\\n Starting a scan for a domain that already has a pending scan from the last 5 minutes returns that scan instead of starting a new one.

### Example

```typescript
import {
    AgentReadinessScansApi,
    Configuration,
    AgentReadinessV1ScansRunScanRequest
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgentReadinessScansApi(configuration);

let agentReadinessV1ScansRunScanRequest: AgentReadinessV1ScansRunScanRequest; //

const { status, data } = await apiInstance.runAgentReadinessScanV1(
    agentReadinessV1ScansRunScanRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agentReadinessV1ScansRunScanRequest** | **AgentReadinessV1ScansRunScanRequest**|  | |


### Return type

**AgentReadinessV1ScansScanResource**

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

