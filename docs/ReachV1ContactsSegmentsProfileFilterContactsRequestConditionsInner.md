# ReachV1ContactsSegmentsProfileFilterContactsRequestConditionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attribute** | **string** | A built-in contact attribute, or &#x60;cf:{fieldUuid}&#x60; to target a custom contact field. Which operators are accepted depends on the attribute, so read the segment filter attributes endpoint for the authoritative list. | [default to undefined]
**operator** | **string** |  | [default to undefined]
**value** | **string** | Always a string, including for numeric and date comparisons | [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsProfileFilterContactsRequestConditionsInner } from '@hostinger/sdk';

const instance: ReachV1ContactsSegmentsProfileFilterContactsRequestConditionsInner = {
    attribute,
    operator,
    value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
