# ReachV1ContactsSegmentsSegmentFilterAttributeResource

One attribute a segment condition can filter on.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Value to send as the condition &#x60;attribute&#x60;. | [optional] [default to undefined]
**type** | **string** | Where the attribute is sourced from. | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**operators** | [**{ [key: string]: ReachV1ContactsSegmentsSegmentFilterOperatorResource; }**](ReachV1ContactsSegmentsSegmentFilterOperatorResource.md) | Operators this attribute accepts, keyed by operator name. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsSegmentFilterAttributeResource } from 'hostinger-api-sdk';

const instance: ReachV1ContactsSegmentsSegmentFilterAttributeResource = {
    name,
    type,
    description,
    operators,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
