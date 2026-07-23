# BillingV1OrderPurchaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **number** | Payment method ID, default will be used if not provided | [optional] [default to undefined]
**items** | [**Array&lt;BillingV1OrderPurchaseRequestItemsInner&gt;**](BillingV1OrderPurchaseRequestItemsInner.md) | Catalog price items to purchase | [default to undefined]
**coupons** | **Array&lt;any&gt;** | Discount coupon codes | [optional] [default to undefined]

## Example

```typescript
import { BillingV1OrderPurchaseRequest } from 'hostinger-api-sdk';

const instance: BillingV1OrderPurchaseRequest = {
    payment_method_id,
    items,
    coupons,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
