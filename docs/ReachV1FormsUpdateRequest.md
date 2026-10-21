# ReachV1FormsUpdateRequest

Rename a form and/or change its status. Send at least one field.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Form name. Letters, digits, spaces and - . \&#39; _ only. | [optional] [default to undefined]
**status** | **string** | &#x60;active&#x60; takes the form live, &#x60;paused&#x60; and &#x60;draft&#x60; stop it accepting submissions. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1FormsUpdateRequest } from '@hostinger/sdk';

const instance: ReachV1FormsUpdateRequest = {
    name,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
