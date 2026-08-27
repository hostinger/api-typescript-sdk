# ReachV1ContactsFieldsStoreRequest

Define a custom contact field for the profile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Immutable once the field exists | [default to undefined]
**label** | **string** |  | [default to undefined]
**_options** | **Array&lt;string&gt;** | Required for single_choice and multi_choice, ignored for the scalar types. Labels must be unique regardless of casing. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsFieldsStoreRequest } from '@hostinger/sdk';

const instance: ReachV1ContactsFieldsStoreRequest = {
    type,
    label,
    _options,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
