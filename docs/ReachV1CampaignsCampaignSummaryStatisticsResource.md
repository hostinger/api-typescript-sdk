# ReachV1CampaignsCampaignSummaryStatisticsResource

Headline engagement rates. The statistics endpoint carries the full breakdown.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_sent** | **number** | Emails sent for this campaign, and the denominator of the rates below. | [optional] [default to undefined]
**open_rate** | **number** | Percentage of sent emails that were opened. | [optional] [default to undefined]
**click_rate** | **number** | Percentage of sent emails that got a click. | [optional] [default to undefined]
**click_to_open_rate** | **number** | Percentage of the contacts who opened that went on to click. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsCampaignSummaryStatisticsResource } from 'hostinger-api-sdk';

const instance: ReachV1CampaignsCampaignSummaryStatisticsResource = {
    total_sent,
    open_rate,
    click_rate,
    click_to_open_rate,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
