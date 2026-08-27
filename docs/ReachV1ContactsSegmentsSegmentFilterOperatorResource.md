# ReachV1ContactsSegmentsSegmentFilterOperatorResource

One operator an attribute accepts, and the value format it expects.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**operator** | **string** | Value to send as the condition &#x60;operator&#x60;. | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**input_type** | **string** | Shape of the value this operator expects, useful for rendering an input. | [optional] [default to undefined]
**example** | **string** | An example value in the format this operator expects. | [optional] [default to undefined]
**enum_values** | **{ [key: string]: string; }** | The values this operator accepts, keyed by the value to send. Only present when the operator is constrained to a fixed set, such as a tag or campaign picker. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsSegmentsSegmentFilterOperatorResource } from '@hostinger/sdk';

const instance: ReachV1ContactsSegmentsSegmentFilterOperatorResource = {
    operator,
    description,
    input_type,
    example,
    enum_values,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
