# AgencyHostingWordPressApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**changeWordPressVersionV1**](#changewordpressversionv1) | **PATCH** /api/agency-hosting/v1/websites/{website_uid}/wordpress/settings/version | Change WordPress version|
|[**getWordPressSettingsV1**](#getwordpresssettingsv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/wordpress/settings | Get WordPress settings|
|[**listAvailableWordPressVersionsV1**](#listavailablewordpressversionsv1) | **GET** /api/agency-hosting/v1/websites/{website_uid}/wordpress/settings/versions | List available WordPress versions|

# **changeWordPressVersionV1**
> CommonSuccessEmptyResource changeWordPressVersionV1(agencyHostingV1WordPressChangeVersionRequest)

Changes the installed WordPress core version on an Agency Plan website to one of the versions available for installation.

### Example

```typescript
import {
    AgencyHostingWordPressApi,
    Configuration,
    AgencyHostingV1WordPressChangeVersionRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWordPressApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1WordPressChangeVersionRequest: AgencyHostingV1WordPressChangeVersionRequest; //

const { status, data } = await apiInstance.changeWordPressVersionV1(
    websiteUid,
    agencyHostingV1WordPressChangeVersionRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1WordPressChangeVersionRequest** | **AgencyHostingV1WordPressChangeVersionRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


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

# **getWordPressSettingsV1**
> AgencyHostingV1WordPressSettingsResource getWordPressSettingsV1()

Returns the current WordPress settings for an Agency Plan website: installed core version, LiteSpeed Cache plugin status, object cache status, and maintenance mode status.

### Example

```typescript
import {
    AgencyHostingWordPressApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWordPressApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.getWordPressSettingsV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**AgencyHostingV1WordPressSettingsResource**

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

# **listAvailableWordPressVersionsV1**
> Array<AgencyHostingV1WordPressVersionResource> listAvailableWordPressVersionsV1()

Lists the WordPress core versions available for installation on an Agency Plan website.

### Example

```typescript
import {
    AgencyHostingWordPressApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWordPressApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)

const { status, data } = await apiInstance.listAvailableWordPressVersionsV1(
    websiteUid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|


### Return type

**Array<AgencyHostingV1WordPressVersionResource>**

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

