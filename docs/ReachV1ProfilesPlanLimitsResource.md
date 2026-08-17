# ReachV1ProfilesPlanLimitsResource

What the plan allows and what is left of it for the current period.  `emails` counts every email sent. `recipients` counts the distinct contacts emailed - it is not the size of the contact list, a contact emailed three times counts once and a contact never emailed does not count at all. `ai_credits` counts the AI generations used, and its limit includes any extra credits bought on top of the plan.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emails** | [**ReachV1ProfilesPlanLimitUsageResource**](ReachV1ProfilesPlanLimitUsageResource.md) |  | [optional] [default to undefined]
**recipients** | [**ReachV1ProfilesPlanLimitUsageResource**](ReachV1ProfilesPlanLimitUsageResource.md) |  | [optional] [default to undefined]
**ai_credits** | [**ReachV1ProfilesPlanLimitUsageResource**](ReachV1ProfilesPlanLimitUsageResource.md) |  | [optional] [default to undefined]
**period_start** | **string** | Start of the current period. Periods are calendar months rather than billing anniversaries, so the counters reset at midnight UTC on the 1st no matter when the subscription started. | [optional] [default to undefined]
**period_end** | **string** | End of the current period, that is the last moment of the calendar month. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesPlanLimitsResource } from 'hostinger-api-sdk';

const instance: ReachV1ProfilesPlanLimitsResource = {
    emails,
    recipients,
    ai_credits,
    period_start,
    period_end,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
