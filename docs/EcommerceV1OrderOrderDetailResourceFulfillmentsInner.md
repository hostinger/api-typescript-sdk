# EcommerceV1OrderOrderDetailResourceFulfillmentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The fulfilment ID. | [optional] [default to undefined]
**created_at** | **string** | ISO timestamp of when the fulfilment was created. | [optional] [default to undefined]
**shipped_at** | **string** | ISO timestamp of when the fulfilment shipped, if known. | [optional] [default to undefined]
**canceled_at** | **string** | ISO timestamp of when the fulfilment was canceled, if any. | [optional] [default to undefined]
**tracking** | [**Array&lt;EcommerceV1OrderOrderDetailResourceFulfillmentsInnerTrackingInner&gt;**](EcommerceV1OrderOrderDetailResourceFulfillmentsInnerTrackingInner.md) | Tracking numbers attached to the fulfilment. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1OrderOrderDetailResourceFulfillmentsInner } from 'hostinger-api-sdk';

const instance: EcommerceV1OrderOrderDetailResourceFulfillmentsInner = {
    id,
    created_at,
    shipped_at,
    canceled_at,
    tracking,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
