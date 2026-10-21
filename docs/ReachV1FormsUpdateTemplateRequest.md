# ReachV1FormsUpdateTemplateRequest

Save the design of a form

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **string** | HTML of the form design. After sanitizing it must still contain a form container (&#x60;data-reach-form&#x60;), an email input (&#x60;data-reach-field&#x3D;\&quot;email\&quot;&#x60;) and a submit button (&#x60;data-reach-submit&#x60;). | [default to undefined]

## Example

```typescript
import { ReachV1FormsUpdateTemplateRequest } from '@hostinger/sdk';

const instance: ReachV1FormsUpdateTemplateRequest = {
    content,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
