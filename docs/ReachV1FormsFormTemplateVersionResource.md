# ReachV1FormsFormTemplateVersionResource

The stored version of a saved form design.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**path** | **string** | Storage path of the template HTML, relative to the storage directory of this profile. | [optional] [default to undefined]
**edit_type** | **string** | Whether the design was saved by hand or by the AI builder. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1FormsFormTemplateVersionResource } from '@hostinger/sdk';

const instance: ReachV1FormsFormTemplateVersionResource = {
    uuid,
    path,
    edit_type,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
