# ReachV1CampaignsCampaignResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**title** | **string** |  | [optional] [default to undefined]
**subject** | **string** |  | [optional] [default to undefined]
**sender_name** | **string** |  | [optional] [default to undefined]
**sender_email** | **string** |  | [optional] [default to undefined]
**template_uuid** | **string** | The email template this campaign uses. The template title is not exposed. | [optional] [default to undefined]
**status** | **string** | A fully sent campaign is &#x60;publish&#x60;. There is no &#x60;sent&#x60;, &#x60;paused&#x60; or &#x60;archived&#x60; status. | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]
**sent_at** | **string** |  | [optional] [default to undefined]
**scheduled_at** | **string** |  | [optional] [default to undefined]
**statistics** | [**ReachV1CampaignsCampaignSummaryStatisticsResource**](ReachV1CampaignsCampaignSummaryStatisticsResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsCampaignResource } from 'hostinger-api-sdk';

const instance: ReachV1CampaignsCampaignResource = {
    uuid,
    title,
    subject,
    sender_name,
    sender_email,
    template_uuid,
    status,
    type,
    created_at,
    updated_at,
    sent_at,
    scheduled_at,
    statistics,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
