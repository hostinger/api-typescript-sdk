# ReachV1CampaignsCampaignStatisticsResource

Campaign performance. Every count is unique contacts rather than raw events, so a contact who opens the same email five times is counted once.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_sent** | **number** | Emails sent for this campaign, and the denominator of every rate below. | [optional] [default to undefined]
**estimated_total_recipients** | **number** | Recipients this campaign was estimated to reach when sending started. Null for campaigns that have not started sending. | [optional] [default to undefined]
**processed_count** | **number** |  | [optional] [default to undefined]
**delivered_count** | **number** |  | [optional] [default to undefined]
**dropped_count** | **number** |  | [optional] [default to undefined]
**bounced_count** | **number** |  | [optional] [default to undefined]
**soft_bounced_count** | **number** |  | [optional] [default to undefined]
**opened_count** | **number** | Contacts who opened this campaign. | [optional] [default to undefined]
**clicked_count** | **number** | Contacts who clicked a link. Only clicks from contacts who also registered an open count. | [optional] [default to undefined]
**unsubscribed_count** | **number** | Contacts who unsubscribed through this campaign. | [optional] [default to undefined]
**open_rate** | **number** | Percentage of sent emails that were opened. | [optional] [default to undefined]
**click_rate** | **number** | Percentage of sent emails that got a click. | [optional] [default to undefined]
**click_to_open_rate** | **number** | Percentage of the contacts who opened that went on to click. | [optional] [default to undefined]
**unsubscribe_rate** | **number** | Percentage of sent emails that led to an unsubscribe. | [optional] [default to undefined]
**has_bounced_contacts** | **boolean** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsCampaignStatisticsResource } from '@hostinger/sdk';

const instance: ReachV1CampaignsCampaignStatisticsResource = {
    total_sent,
    estimated_total_recipients,
    processed_count,
    delivered_count,
    dropped_count,
    bounced_count,
    soft_bounced_count,
    opened_count,
    clicked_count,
    unsubscribed_count,
    open_rate,
    click_rate,
    click_to_open_rate,
    unsubscribe_rate,
    has_bounced_contacts,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
