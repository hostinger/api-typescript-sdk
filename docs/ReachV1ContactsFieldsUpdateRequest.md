# ReachV1ContactsFieldsUpdateRequest

Rename a custom contact field and, for the choice types, replace its option set. The field type and slug are immutable.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **string** |  | [default to undefined]
**_options** | [**Array&lt;ReachV1ContactsFieldsUpdateRequestOptionsInner&gt;**](ReachV1ContactsFieldsUpdateRequestOptionsInner.md) | Replaces the option set when provided. Entries carrying a uuid are kept and relabelled, entries without one are created, and any existing option missing from the list is deleted along with the values contacts hold for it. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsFieldsUpdateRequest } from '@hostinger/sdk';

const instance: ReachV1ContactsFieldsUpdateRequest = {
    label,
    _options,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
