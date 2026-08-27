# ReachV1AutomationsStepsAutomationStepResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**parent_uuid** | **string** | The step this one branches from. Null for the entry point of the workflow. | [optional] [default to undefined]
**step_order** | **number** | Position of this step among the steps sharing its parent. | [optional] [default to undefined]
**type** | **string** | Role of the step in the workflow. A &#x60;conditional&#x60; step branches into several children. | [optional] [default to undefined]
**value** | **string** | The concrete trigger, action, decision or delay this step performs. | [optional] [default to undefined]
**config** | **object** | Step configuration. The shape depends on the value, and is empty for steps that take none. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1AutomationsStepsAutomationStepResource } from '@hostinger/sdk';

const instance: ReachV1AutomationsStepsAutomationStepResource = {
    uuid,
    parent_uuid,
    step_order,
    type,
    value,
    config,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
