# HostingWebsitesApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createWebsiteV1**](#createwebsitev1) | **POST** /api/hosting/v1/websites | Create website|
|[**deleteWebsiteV1**](#deletewebsitev1) | **DELETE** /api/hosting/v1/websites/{domain} | Delete website|
|[**deployStaticSiteArchiveV1**](#deploystaticsitearchivev1) | **POST** /api/hosting/v1/accounts/{username}/websites/{domain}/deploy | Deploy static site archive|
|[**listWebsitesV1**](#listwebsitesv1) | **GET** /api/hosting/v1/websites | List websites|

# **createWebsiteV1**
> CommonSuccessEmptyResource createWebsiteV1(hostingV1WebsitesCreateWebsiteRequest)

Create a new website for the authenticated client.  Provide the domain name and associated order ID to create a new website. The datacenter_code parameter is required when creating the first website on a new hosting plan - this will set up and configure new hosting account in the selected datacenter.  Subsequent websites will be hosted on the same datacenter automatically.  Website creation takes up to a few minutes to complete. Check the websites list endpoint to see when your new website becomes available.

### Example

```typescript
import {
    HostingWebsitesApi,
    Configuration,
    HostingV1WebsitesCreateWebsiteRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingWebsitesApi(configuration);

let hostingV1WebsitesCreateWebsiteRequest: HostingV1WebsitesCreateWebsiteRequest; //

const { status, data } = await apiInstance.createWebsiteV1(
    hostingV1WebsitesCreateWebsiteRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1WebsitesCreateWebsiteRequest** | **HostingV1WebsitesCreateWebsiteRequest**|  | |


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

# **deleteWebsiteV1**
> CommonSuccessEmptyResource deleteWebsiteV1()

This endpoint permanently removes a website and all of its data. This action cannot be undone. Before calling it, make sure the user understands the consequences and explicitly confirms that they want to proceed.  All website files, databases and related configuration will be removed. The hosting plan itself is kept, so a new website can be created on it afterwards.  Supported websites: main and addon domain websites on web hosting plans, and Website Builder websites. Parked domains and subdomains cannot be deleted with this endpoint. The domain must be the exact website domain, not a preview domain or an alias.  Returns 404 when the domain does not exist or does not belong to the authenticated client.  Website removal is processed asynchronously and can take a few minutes to complete. The response returns before the removal finishes.

### Example

```typescript
import {
    HostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingWebsitesApi(configuration);

let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.deleteWebsiteV1(
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deployStaticSiteArchiveV1**
> CommonSuccessEmptyResource deployStaticSiteArchiveV1(hostingV1WebsitesDeployArchiveRequest)

Deploy a static application from an archive file.  WARNING: this overwrites the website\'s existing contents and cannot be undone — verify this is intended before calling this endpoint.  This endpoint allows you to deploy a static application from an archive file that has been uploaded to the website\'s directory.  This only works for static sites (pre-built HTML/CSS/JS with no build step). For Node.js applications, use `Create NodeJS build from archive` instead, or `Start Node.js build` if the archive is already uploaded. For WordPress sites, use `Import WordPress website`.

### Example

```typescript
import {
    HostingWebsitesApi,
    Configuration,
    HostingV1WebsitesDeployArchiveRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingWebsitesApi(configuration);

let username: string; // (default to undefined)
let domain: string; //Domain name (default to undefined)
let hostingV1WebsitesDeployArchiveRequest: HostingV1WebsitesDeployArchiveRequest; //

const { status, data } = await apiInstance.deployStaticSiteArchiveV1(
    username,
    domain,
    hostingV1WebsitesDeployArchiveRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **hostingV1WebsitesDeployArchiveRequest** | **HostingV1WebsitesDeployArchiveRequest**|  | |
| **username** | [**string**] |  | defaults to undefined|
| **domain** | [**string**] | Domain name | defaults to undefined|


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
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **listWebsitesV1**
> HostingListWebsitesV1200Response listWebsitesV1()

Retrieve a paginated list of websites (CloudLinux, Builder, and Horizons) accessible to the authenticated client.  This endpoint returns websites from your hosting accounts as well as websites from other client hosting accounts that have shared access with you.  Each website includes a `website_type` field describing the type of website detected on the underlying platform (`wordpress`, `builder`, `horizons`, `nodejs`, or `other`). Some fields, such as `vhost_type`, `username`, and `root_directory`, only apply to CloudLinux websites and are null for other platforms.  Use the available query parameters to filter results by username, order ID, enabled status, or domain name for more targeted results.

### Example

```typescript
import {
    HostingWebsitesApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new HostingWebsitesApi(configuration);

let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let username: string; //Filter by specific username (optional) (default to undefined)
let orderId: number; //Order ID (optional) (default to undefined)
let isEnabled: boolean; //Filter by enabled status (optional) (default to undefined)
let domain: string; //Filter by domain name (exact match) (optional) (default to undefined)

const { status, data } = await apiInstance.listWebsitesV1(
    page,
    perPage,
    username,
    orderId,
    isEnabled,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **username** | [**string**] | Filter by specific username | (optional) defaults to undefined|
| **orderId** | [**number**] | Order ID | (optional) defaults to undefined|
| **isEnabled** | [**boolean**] | Filter by enabled status | (optional) defaults to undefined|
| **domain** | [**string**] | Filter by domain name (exact match) | (optional) defaults to undefined|


### Return type

**HostingListWebsitesV1200Response**

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

