# ReachV1FormsFormDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**status** | **string** | A &#x60;paused&#x60; form keeps its template online but stops accepting submissions. | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**template** | [**ReachV1FormsFormTemplateDetailsResource**](ReachV1FormsFormTemplateDetailsResource.md) |  | [optional] [default to undefined]
**tags** | [**Array&lt;ReachV1FormsFormTagResource&gt;**](ReachV1FormsFormTagResource.md) | Tags applied to every contact this form captures. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1FormsFormDetailsResource } from '@hostinger/sdk';

const instance: ReachV1FormsFormDetailsResource = {
    uuid,
    name,
    status,
    type,
    template,
    tags,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
