# AgencyHostingCacheApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**clearAgencyPlanWebsiteCacheV1**](#clearagencyplanwebsitecachev1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid}/cache | Clear Agency Plan website cache|

# **clearAgencyPlanWebsiteCacheV1**
> CommonSuccessEmptyResource clearAgencyPlanWebsiteCacheV1()

Clears cache for all domains associated with an Agency Plan website, including its preview domain.  This operation clears all cache types for the website.

### Example

```typescript
import {
    AgencyHostingCacheApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingCacheApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.clearAgencyPlanWebsiteCacheV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


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

