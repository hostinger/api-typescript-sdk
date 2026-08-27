# ReachV1FormsFormTemplateDetailsResource

The rendered form template. There is no ready-made embed snippet - either serve the HTML behind `url` or build your own embed around the form uuid. All fields stay null until the template has been generated.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**path** | **string** | Storage path of the template HTML, relative to the storage directory of this profile. &#x60;url&#x60; already includes that prefix, so prefer it unless you resolve storage paths yourself. | [optional] [default to undefined]
**url** | **string** | Publicly reachable URL of the template HTML. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1FormsFormTemplateDetailsResource } from '@hostinger/sdk';

const instance: ReachV1FormsFormTemplateDetailsResource = {
    uuid,
    path,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
