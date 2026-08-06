# ReachV1ContactsBulkStoreRequest

Create many contacts in one call

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contacts** | [**Array&lt;ReachV1ContactsBulkStoreRequestContactsInner&gt;**](ReachV1ContactsBulkStoreRequestContactsInner.md) |  | [default to undefined]
**tag_uuids** | **Array&lt;string&gt;** | Existing tags to attach to every created contact | [optional] [default to undefined]
**note** | **string** | Note applied to every created contact | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsBulkStoreRequest } from 'hostinger-api-sdk';

const instance: ReachV1ContactsBulkStoreRequest = {
    contacts,
    tag_uuids,
    note,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
