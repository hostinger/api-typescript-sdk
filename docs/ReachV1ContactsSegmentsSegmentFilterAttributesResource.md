# ReachV1ContactsSegmentsSegmentFilterAttributesResource

The vocabulary a segment condition can be built from, for one profile.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attributes** | [**{ [key: string]: ReachV1ContactsSegmentsSegmentFilterAttributeResource; }**](ReachV1ContactsSegmentsSegmentFilterAttributeResource.md) | Every attribute a condition can filter on, keyed by the value to send as &#x60;attribute&#x60;. Custom contact fields are keyed &#x60;cf:{fieldUuid}&#x60;, tags and campaigns by their uuid, so the keys are not a fixed list and should be read from this response rather than hardcoded. | [optional] [default to undefined]
**logic_operators** | **{ [key: string]: string; }** | The values accepted by &#x60;logic&#x60; when a segment combines several conditions. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsSegmentFilterAttributesResource } from '@hostinger/sdk';

const instance: ReachV1ContactsSegmentsSegmentFilterAttributesResource = {
    attributes,
    logic_operators,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
