# ReachV1ContactsSegmentsProfileUpdateRequest

Rename a segment and/or replace the conditions that define it

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**conditions** | [**Array&lt;ReachV1ContactsSegmentsProfileStoreRequestConditionsInner&gt;**](ReachV1ContactsSegmentsProfileStoreRequestConditionsInner.md) | Replaces the existing conditions entirely. Omit to keep the current ones. | [optional] [default to undefined]
**logic** | **string** | How to combine multiple conditions. Required when conditions are given. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsProfileUpdateRequest } from 'hostinger-api-sdk';

const instance: ReachV1ContactsSegmentsProfileUpdateRequest = {
    name,
    conditions,
    logic,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
