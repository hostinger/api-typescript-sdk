# ReachV1AutomationsAutomationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**status** | **string** | There is no &#x60;completed&#x60; status. Use &#x60;events.completed&#x60; to see how many contacts finished. | [optional] [default to undefined]
**type** | **string** | What kind of workflow this is. &#x60;custom&#x60; automations are the ones built from scratch. | [optional] [default to undefined]
**config** | **object** | Trigger configuration of the automation. The shape depends on the type. | [optional] [default to undefined]
**events** | [**ReachV1AutomationsAutomationEventsResource**](ReachV1AutomationsAutomationEventsResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1AutomationsAutomationResource } from '@hostinger/sdk';

const instance: ReachV1AutomationsAutomationResource = {
    uuid,
    name,
    status,
    type,
    config,
    events,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
