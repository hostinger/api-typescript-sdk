# ReachProfilesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**listProfilesV1**](#listprofilesv1) | **GET** /api/reach/v1/profiles | List Profiles|

# **listProfilesV1**
> Array<ReachV1ProfilesProfileResource> listProfilesV1()

This endpoint returns all profiles available to the client, including their basic information.

### Example

```typescript
import {
    ReachProfilesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachProfilesApi(configuration);

const { status, data } = await apiInstance.listProfilesV1();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<ReachV1ProfilesProfileResource>**

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

