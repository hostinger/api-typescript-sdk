# ReachV1AutomationsAutomationEventsResource

Counts of contacts moving through the automation.  These are not email engagement metrics. Automations expose no sent, open or click counters - use the campaign statistics endpoint for those.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**started** | **number** | Contacts that ever entered the automation, including those that already left it. | [optional] [default to undefined]
**in_progress** | **number** | Contacts currently moving through the automation, including those waiting on a delay step. | [optional] [default to undefined]
**completed** | **number** | Contacts that reached the end of the workflow. | [optional] [default to undefined]
**failed** | **number** | Contacts whose journey through the automation errored and stopped. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1AutomationsAutomationEventsResource } from '@hostinger/sdk';

const instance: ReachV1AutomationsAutomationEventsResource = {
    started,
    in_progress,
    completed,
    failed,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
