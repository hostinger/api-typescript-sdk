# ReachV1ProfilesPlanLimitUsageResource

Allowance, consumption and headroom of a single plan limit for the current period.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **number** | The allowance for the current period. | [optional] [default to undefined]
**used** | **number** | How much of the allowance has been consumed so far. | [optional] [default to undefined]
**remaining** | **number** | Headroom left. Floors at 0, so it never reports a negative overage. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesPlanLimitUsageResource } from '@hostinger/sdk';

const instance: ReachV1ProfilesPlanLimitUsageResource = {
    limit,
    used,
    remaining,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
