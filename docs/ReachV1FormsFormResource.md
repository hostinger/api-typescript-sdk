# ReachV1FormsFormResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**status** | **string** | A &#x60;paused&#x60; form keeps its template online but stops accepting submissions. | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**template** | [**ReachV1FormsFormTemplateResource**](ReachV1FormsFormTemplateResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1FormsFormResource } from 'hostinger-api-sdk';

const instance: ReachV1FormsFormResource = {
    uuid,
    name,
    status,
    type,
    template,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
