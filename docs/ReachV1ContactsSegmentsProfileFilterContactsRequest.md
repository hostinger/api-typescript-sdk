# ReachV1ContactsSegmentsProfileFilterContactsRequest

Conditions to preview, in the same shape accepted when creating a segment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conditions** | [**Array&lt;ReachV1ContactsSegmentsProfileFilterContactsRequestConditionsInner&gt;**](ReachV1ContactsSegmentsProfileFilterContactsRequestConditionsInner.md) | Conditions a contact must satisfy to appear in the preview | [default to undefined]
**logic** | **string** | How to combine multiple conditions | [default to undefined]
**page** | **number** | Page number | [optional] [default to undefined]
**per_page** | **number** | Number of items per page | [optional] [default to undefined]
**search** | **string** | Narrow the preview to contacts whose email matches | [optional] [default to undefined]
**sort_by** | **string** |  | [optional] [default to undefined]
**sort_direction** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsProfileFilterContactsRequest } from 'hostinger-api-sdk';

const instance: ReachV1ContactsSegmentsProfileFilterContactsRequest = {
    conditions,
    logic,
    page,
    per_page,
    search,
    sort_by,
    sort_direction,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
