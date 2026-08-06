# ReachV1ContactsFieldsContactFieldResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**label** | **string** |  | [optional] [default to undefined]
**slug** | **string** | Derived from the label on creation and immutable afterwards | [optional] [default to undefined]
**_options** | [**Array&lt;ReachV1ContactsFieldsContactFieldOptionResource&gt;**](ReachV1ContactsFieldsContactFieldOptionResource.md) | Available choices. Always empty for the scalar field types. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsFieldsContactFieldResource } from 'hostinger-api-sdk';

const instance: ReachV1ContactsFieldsContactFieldResource = {
    uuid,
    type,
    label,
    slug,
    _options,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
