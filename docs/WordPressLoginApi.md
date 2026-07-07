# WordPressLoginApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createLoginLinksV1**](#createloginlinksv1) | **POST** /api/hosting/v1/accounts/{username}/wordpress/{software}/login/links | Create login links|

# **createLoginLinksV1**
> WordPressV1LoginLoginLinksResource createLoginLinksV1()

Create temporary auto-login links for the specified WordPress installation.  Provide the WordPress installation (software) identifier in the path. It can be obtained from GET /api/hosting/v1/wordpress/installations (the `id` field).

### Example

```typescript
import {
    WordPressLoginApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new WordPressLoginApi(configuration);

let username: string; // (default to undefined)
let software: string; //WordPress installation (software) identifier (default to undefined)

const { status, data } = await apiInstance.createLoginLinksV1(
    username,
    software
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **username** | [**string**] |  | defaults to undefined|
| **software** | [**string**] | WordPress installation (software) identifier | defaults to undefined|


### Return type

**WordPressV1LoginLoginLinksResource**

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

