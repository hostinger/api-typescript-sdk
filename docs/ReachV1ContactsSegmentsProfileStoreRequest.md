# ReachV1ContactsSegmentsProfileStoreRequest

Create a segment from a set of conditions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**conditions** | [**Array&lt;ReachV1ContactsSegmentsProfileStoreRequestConditionsInner&gt;**](ReachV1ContactsSegmentsProfileStoreRequestConditionsInner.md) | Conditions a contact must satisfy to fall into the segment | [default to undefined]
**logic** | **string** | How to combine multiple conditions | [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsProfileStoreRequest } from 'hostinger-api-sdk';

const instance: ReachV1ContactsSegmentsProfileStoreRequest = {
    name,
    conditions,
    logic,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
