# ReachCampaignsApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**getCampaignDetailsV1**](#getcampaigndetailsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/campaigns/{campaignUuid} | Get campaign details|
|[**getCampaignPerformanceV1**](#getcampaignperformancev1) | **GET** /api/reach/v1/profiles/{profileUuid}/campaigns/{campaignUuid}/statistics | Get campaign performance|
|[**listCampaignsV1**](#listcampaignsv1) | **GET** /api/reach/v1/profiles/{profileUuid}/campaigns | List campaigns|

# **getCampaignDetailsV1**
> ReachV1CampaignsCampaignDetailsResource getCampaignDetailsV1()

Get a single campaign with its sender, subject, template reference, targeting and delivery progress.  This describes how the campaign was set up and how far it has got. For opens, clicks and unsubscribes use the campaign statistics endpoint.

### Example

```typescript
import {
    ReachCampaignsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachCampaignsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let campaignUuid: string; //Campaign uuid parameter (default to undefined)

const { status, data } = await apiInstance.getCampaignDetailsV1(
    profileUuid,
    campaignUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **campaignUuid** | [**string**] | Campaign uuid parameter | defaults to undefined|


### Return type

**ReachV1CampaignsCampaignDetailsResource**

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

# **getCampaignPerformanceV1**
> ReachV1CampaignsCampaignStatisticsResource getCampaignPerformanceV1()

Get the performance of a campaign: delivery, opens, clicks and unsubscribes, with the matching rates.  Every count is unique contacts rather than raw events, so a contact who opens the same email five times is counted once.

### Example

```typescript
import {
    ReachCampaignsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachCampaignsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let campaignUuid: string; //Campaign uuid parameter (default to undefined)

const { status, data } = await apiInstance.getCampaignPerformanceV1(
    profileUuid,
    campaignUuid
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **campaignUuid** | [**string**] | Campaign uuid parameter | defaults to undefined|


### Return type

**ReachV1CampaignsCampaignStatisticsResource**

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

# **listCampaignsV1**
> ReachListCampaignsV1200Response listCampaignsV1()

Get a paginated list of the campaigns in a profile.  Each campaign carries its headline engagement rates. Filter by status to find drafts, scheduled, sending or sent campaigns, keeping in mind that a fully sent campaign has the status `publish`. By default only regular campaigns are returned - pass `type` to get the emails sent by automations or the double opt-in confirmations instead.

### Example

```typescript
import {
    ReachCampaignsApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new ReachCampaignsApi(configuration);

let profileUuid: string; //Profile uuid parameter (default to undefined)
let status: 'draft' | 'scheduled' | 'sending' | 'publish' | 'failed'; //Filter campaigns by status.  A fully sent campaign has the status `publish`. There is no `sent` status, and campaigns can be neither paused nor archived. (optional) (default to undefined)
let type: 'campaign' | 'automation' | 'double_opt_in'; //Filter campaigns by type.  Defaults to `campaign`, which leaves out the emails sent by automations and the double opt-in confirmations. (optional) (default to 'campaign')
let sortDirection: 'asc' | 'desc'; //Order campaigns by creation date. Newest first unless set to `asc`. (optional) (default to undefined)
let page: number; //Page number (optional) (default to undefined)
let perPage: number; //Number of items per page (optional) (default to 25)

const { status, data } = await apiInstance.listCampaignsV1(
    profileUuid,
    status,
    type,
    sortDirection,
    page,
    perPage
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileUuid** | [**string**] | Profile uuid parameter | defaults to undefined|
| **status** | [**&#39;draft&#39; | &#39;scheduled&#39; | &#39;sending&#39; | &#39;publish&#39; | &#39;failed&#39;**]**Array<&#39;draft&#39; &#124; &#39;scheduled&#39; &#124; &#39;sending&#39; &#124; &#39;publish&#39; &#124; &#39;failed&#39;>** | Filter campaigns by status.  A fully sent campaign has the status &#x60;publish&#x60;. There is no &#x60;sent&#x60; status, and campaigns can be neither paused nor archived. | (optional) defaults to undefined|
| **type** | [**&#39;campaign&#39; | &#39;automation&#39; | &#39;double_opt_in&#39;**]**Array<&#39;campaign&#39; &#124; &#39;automation&#39; &#124; &#39;double_opt_in&#39;>** | Filter campaigns by type.  Defaults to &#x60;campaign&#x60;, which leaves out the emails sent by automations and the double opt-in confirmations. | (optional) defaults to 'campaign'|
| **sortDirection** | [**&#39;asc&#39; | &#39;desc&#39;**]**Array<&#39;asc&#39; &#124; &#39;desc&#39;>** | Order campaigns by creation date. Newest first unless set to &#x60;asc&#x60;. | (optional) defaults to undefined|
| **page** | [**number**] | Page number | (optional) defaults to undefined|
| **perPage** | [**number**] | Number of items per page | (optional) defaults to 25|


### Return type

**ReachListCampaignsV1200Response**

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

