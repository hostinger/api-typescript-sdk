# ReachV1ProfilesFeaturesPlanFeatureResource

Whether a single plan feature can be used on the profile.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**feature** | **string** |  | [optional] [default to undefined]
**is_available** | **boolean** | Whether the feature can be used right now. | [optional] [default to undefined]
**is_locked** | **boolean** | Whether the feature sits outside the base plan and needs an upgrade. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesFeaturesPlanFeatureResource } from 'hostinger-api-sdk';

const instance: ReachV1ProfilesFeaturesPlanFeatureResource = {
    feature,
    is_available,
    is_locked,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
