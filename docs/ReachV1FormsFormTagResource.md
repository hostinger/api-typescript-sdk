# ReachV1FormsFormTagResource

A tag applied to every contact this form captures.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**value** | **string** |  | [optional] [default to undefined]
**type** | **string** | How the tag came about. &#x60;custom&#x60; covers the tags you create yourself, &#x60;import&#x60; the ones added by contact imports, and &#x60;form&#x60; and &#x60;system&#x60; the ones Reach creates on its own. Every form gets a &#x60;form:{name}&#x60; tag when it is created. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1FormsFormTagResource } from '@hostinger/sdk';

const instance: ReachV1FormsFormTagResource = {
    uuid,
    value,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
