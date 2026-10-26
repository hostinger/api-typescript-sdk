# ReachV1ContactsBulkStoreRequestContactsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** |  | [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**surname** | **string** |  | [optional] [default to undefined]
**phone** | **string** | Phone number in E.164 format (leading \&quot;+\&quot; then 7-15 digits) | [optional] [default to undefined]
**fields** | [**Array&lt;ReachV1ContactsBulkStoreRequestContactsInnerFieldsInner&gt;**](ReachV1ContactsBulkStoreRequestContactsInnerFieldsInner.md) | Custom field values to set on the contact. For a contact whose email already exists, only fields that have no value yet are filled. Unknown field UUIDs and values that do not match the field type are skipped. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsBulkStoreRequestContactsInner } from '@hostinger/sdk';

const instance: ReachV1ContactsBulkStoreRequestContactsInner = {
    email,
    name,
    surname,
    phone,
    fields,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
