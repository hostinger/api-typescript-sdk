# ReachV1ContactsTagsManageContactsRequest

Contacts to assign to, or remove from, a tag

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contact_uuids** | **Array&lt;string&gt;** | Contacts to apply the change to. Required unless all_contacts is true. | [optional] [default to undefined]
**all_contacts** | **boolean** | Apply to every contact in the profile | [optional] [default to false]

## Example

```typescript
import { ReachV1ContactsTagsManageContactsRequest } from 'hostinger-api-sdk';

const instance: ReachV1ContactsTagsManageContactsRequest = {
    contact_uuids,
    all_contacts,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
