# AgencyHostingDomainsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**changeAgencyPlanWebsiteDomainV1**](#changeagencyplanwebsitedomainv1) | **PUT** /api/agency-hosting/v1/websites/{website_uid}/domains/{from_domain} | Change Agency Plan website domain|
|[**linkDomainToAgencyPlanWebsiteV1**](#linkdomaintoagencyplanwebsitev1) | **POST** /api/agency-hosting/v1/websites/{website_uid}/domains | Link domain to Agency Plan website|
|[**listAgencyPlanDomainsV1**](#listagencyplandomainsv1) | **GET** /api/agency-hosting/v1/domains | List Agency Plan domains|
|[**unlinkDomainFromAgencyPlanWebsiteV1**](#unlinkdomainfromagencyplanwebsitev1) | **DELETE** /api/agency-hosting/v1/websites/{website_uid}/domains/{domain} | Unlink domain from Agency Plan website|

# **changeAgencyPlanWebsiteDomainV1**
> CommonSuccessEmptyResource changeAgencyPlanWebsiteDomainV1(agencyHostingV1DomainsChangeDomainRequest)

Changes the primary domain for an Agency Plan website.  Provide the current domain in the path and the new domain in the request body. Set domain to null to revert to the temporary domain.

### Example

```typescript
import {
    AgencyHostingDomainsApi,
    Configuration,
    AgencyHostingV1DomainsChangeDomainRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDomainsApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let fromDomain: string; //Current domain name to change from (default to undefined)
let agencyHostingV1DomainsChangeDomainRequest: AgencyHostingV1DomainsChangeDomainRequest; //

const { status, data } = await apiInstance.changeAgencyPlanWebsiteDomainV1(
    websiteUid,
    fromDomain,
    agencyHostingV1DomainsChangeDomainRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1DomainsChangeDomainRequest** | **AgencyHostingV1DomainsChangeDomainRequest**|  | |
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
| **fromDomain** | [**string**] | Current domain name to change from | defaults to undefined|


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

# **linkDomainToAgencyPlanWebsiteV1**
> CommonSuccessEmptyResource linkDomainToAgencyPlanWebsiteV1(agencyHostingV1DomainsLinkDomainRequest)

Links a domain to the specified Agency Plan website so it can serve traffic for that domain.

### Example

```typescript
import {
    AgencyHostingDomainsApi,
    Configuration,
    AgencyHostingV1DomainsLinkDomainRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDomainsApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let agencyHostingV1DomainsLinkDomainRequest: AgencyHostingV1DomainsLinkDomainRequest; //

const { status, data } = await apiInstance.linkDomainToAgencyPlanWebsiteV1(
    websiteUid,
    agencyHostingV1DomainsLinkDomainRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **agencyHostingV1DomainsLinkDomainRequest** | **AgencyHostingV1DomainsLinkDomainRequest**|  | |
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

# **listAgencyPlanDomainsV1**
> AgencyHostingListAgencyPlanDomainsV1200Response listAgencyPlanDomainsV1()

Returns a paginated list of domains associated with Agency Plan websites accessible to the authenticated client.  Use the website_uuids filter to narrow results to specific websites.

### Example

```typescript
import {
    AgencyHostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDomainsApi(configuration);

let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)
let websiteUuids: Array<string>; //Filter by website UIDs (optional) (default to undefined)

const { status, data } = await apiInstance.listAgencyPlanDomainsV1(
    page,
    perPage,
    websiteUuids
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|
| **websiteUuids** | **Array&lt;string&gt;** | Filter by website UIDs | (optional) defaults to undefined|


### Return type

**AgencyHostingListAgencyPlanDomainsV1200Response**

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

# **unlinkDomainFromAgencyPlanWebsiteV1**
> CommonSuccessEmptyResource unlinkDomainFromAgencyPlanWebsiteV1()

Unlinks a domain from the specified Agency Plan website.  The website stops serving traffic on this domain immediately.  Website files and database are preserved, and any other linked domains remain accessible.  If this is the only domain on the website, unlinking leaves the website without an accessible domain.

### Example

```typescript
import {
    AgencyHostingDomainsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new AgencyHostingDomainsApi(configuration);

let websiteUid: string; //Agency Plan website UID (default to undefined)
let domain: string; //Domain name (default to undefined)

const { status, data } = await apiInstance.unlinkDomainFromAgencyPlanWebsiteV1(
    websiteUid,
    domain
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **websiteUid** | [**string**] | Agency Plan website UID | defaults to undefined|
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
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

