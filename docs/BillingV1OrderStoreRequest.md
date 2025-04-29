# BillingV1OrderStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **number** | Payment method ID | [default to undefined]
**items** | [**Array&lt;BillingV1OrderStoreRequestItemsInner&gt;**](BillingV1OrderStoreRequestItemsInner.md) |  | [default to undefined]
**coupons** | **Array&lt;any&gt;** | Discount coupon codes | [optional] [default to undefined]

## Example

```typescript
import { BillingV1OrderStoreRequest } from 'hostinger-api-sdk';

const instance: BillingV1OrderStoreRequest = {
    payment_method_id,
    items,
    coupons,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
