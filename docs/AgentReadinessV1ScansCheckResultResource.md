# AgentReadinessV1ScansCheckResultResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**check_id** | **string** | Check ID, as listed by the &#x60;List checks&#x60; operation | [default to undefined]
**category** | **string** | Category the check belongs to | [default to undefined]
**status** | **string** | Check outcome. &#x60;not_applicable&#x60; and &#x60;error&#x60; checks do not count towards the category score. | [default to undefined]
**earned** | **number** | Points earned by this check | [default to undefined]
**possible** | **number** | Points this check can earn | [default to undefined]
**evidence** | **string** | What the scanner observed | [default to undefined]
**fix** | **string** | How to improve the result, or null when there is nothing to fix | [default to undefined]

## Example

```typescript
import { AgentReadinessV1ScansCheckResultResource } from '@hostinger/sdk';

const instance: AgentReadinessV1ScansCheckResultResource = {
    check_id,
    category,
    status,
    earned,
    possible,
    evidence,
    fix,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
