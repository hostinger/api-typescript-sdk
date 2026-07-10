# AgencyHostingWebsiteSetupsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getAgencyPlanWebsiteSetupStatusV1**](#getagencyplanwebsitesetupstatusv1) | **GET** /api/agency-hosting/v1/orders/{order_id}/websites/setups/{setup_uuid} | Get Agency Plan website setup status|
|[**provisionANewAgencyPlanWebsiteV1**](#provisionanewagencyplanwebsitev1) | **POST** /api/agency-hosting/v1/orders/{order_id}/websites/setups | Provision a new Agency Plan website|

# **getAgencyPlanWebsiteSetupStatusV1**
> AgencyHostingV1SetupsWebsiteSetupStatusResource getAgencyPlanWebsiteSetupStatusV1()

Returns the current status of an Agency Plan website setup started via the setups endpoint.  Poll this endpoint using the `setup_uuid` returned from the provisioning request until `status` becomes `completed`, at which point `website_uid` identifies the new website.

### Example

```typescript
import {
    AgencyHostingWebsiteSetupsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsiteSetupsApi(configuration);

let orderId: number; //Agency Plan order ID (default to undefined)
let setupUuid: string; //Website setup UUID (default to undefined)

const { status, data } = await apiInstance.getAgencyPlanWebsiteSetupStatusV1(
    orderId,
    setupUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **orderId** | [**number**] | Agency Plan order ID | defaults to undefined|
| **setupUuid** | [**string**] | Website setup UUID | defaults to undefined|


### Return type

**AgencyHostingV1SetupsWebsiteSetupStatusResource**

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

# **provisionANewAgencyPlanWebsiteV1**
> AgencyHostingV1SetupsWebsiteSetupResource provisionANewAgencyPlanWebsiteV1(agencyHostingV1SetupsCreateSetupRequest)

Provisions a new website on one of your Agency Plan hosting orders.  Choose the datacenter, stack (`flavor`), and PHP version for the site. Optionally attach your own `domain` — omit it, set it to `null`, or leave it unavailable and a free `*.hostingersite.com` subdomain is generated instead — and/or install WordPress by supplying the `wordpress` details (admin account, site title, and language).  Common setups: - **Plain PHP site**: `flavor` set to `php-fpm`, with `settings.php.version`; omit   `wordpress` and `type`. - **WordPress site**: `flavor` set to the desired WordPress version (e.g. `wp-7.0`), plus   the `wordpress` block (admin account, title, language). - **Static/Node.js frontend app**: `flavor` set to `php-fpm` and `type` set to   `node-static`.  Provisioning runs in the background, so the response returns immediately with a setup UUID that identifies the job. The new website becomes reachable once provisioning finishes.

### Example

```typescript
import {
    AgencyHostingWebsiteSetupsApi,
    Configuration,
    AgencyHostingV1SetupsCreateSetupRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingWebsiteSetupsApi(configuration);

let orderId: number; //Agency Plan order ID (default to undefined)
let agencyHostingV1SetupsCreateSetupRequest: AgencyHostingV1SetupsCreateSetupRequest; //

const { status, data } = await apiInstance.provisionANewAgencyPlanWebsiteV1(
    orderId,
    agencyHostingV1SetupsCreateSetupRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1SetupsCreateSetupRequest** | **AgencyHostingV1SetupsCreateSetupRequest**|  | |
| **orderId** | [**number**] | Agency Plan order ID | defaults to undefined|


### Return type

**AgencyHostingV1SetupsWebsiteSetupResource**

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

