# ReachV1CampaignsCampaignDeliveryResource

Delivery progress. While the campaign is `sending`, `total_sent` climbs towards the estimate.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_sent** | **number** | Emails sent so far. | [optional] [default to undefined]
**estimated_total_recipients** | **number** | Recipients this campaign was estimated to reach when sending started. Null for campaigns that have not started sending. | [optional] [default to undefined]
**subscribers_count** | **number** | Contacts currently targeted by this campaign. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsCampaignDeliveryResource } from 'hostinger-api-sdk';

const instance: ReachV1CampaignsCampaignDeliveryResource = {
    total_sent,
    estimated_total_recipients,
    subscribers_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
