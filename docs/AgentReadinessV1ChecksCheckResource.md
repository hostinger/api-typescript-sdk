# AgentReadinessV1ChecksCheckResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Check ID, as used by &#x60;check_id&#x60; in scan results | [default to undefined]
**name** | **string** | Human-readable check name | [default to undefined]
**category** | **string** | Category the check belongs to | [default to undefined]
**category_label** | **string** | Human-readable category name | [default to undefined]
**weight** | **number** | Points this check can earn | [default to undefined]

## Example

```typescript
import { AgentReadinessV1ChecksCheckResource } from '@hostinger/sdk';

const instance: AgentReadinessV1ChecksCheckResource = {
    id,
    name,
    category,
    category_label,
    weight,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
