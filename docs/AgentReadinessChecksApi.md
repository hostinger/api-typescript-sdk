# AgentReadinessChecksApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listChecksV1**](#listchecksv1) | **GET** /api/agent-readiness/v1/checks | List checks|

# **listChecksV1**
> Array<AgentReadinessV1ChecksCheckResource> listChecksV1()

List every check an agent readiness scan runs, with its name, category and weight.\\n Use it to show the human-readable name of each `check_id` in a scan\'s results.

### Example

```typescript
import {
    AgentReadinessChecksApi,
    Configuration
} from '@hostinger/sdk';

const configuration = new Configuration();
const apiInstance = new AgentReadinessChecksApi(configuration);

const { status, data } = await apiInstance.listChecksV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<AgentReadinessV1ChecksCheckResource>**

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

