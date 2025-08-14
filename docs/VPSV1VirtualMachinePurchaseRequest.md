# VPSV1VirtualMachinePurchaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**item_id** | **string** | Catalog price item ID | [default to undefined]
**payment_method_id** | **number** | Payment method ID, default will be used if not provided | [optional] [default to undefined]
**setup** | [**VPSV1VirtualMachineSetupRequest**](VPSV1VirtualMachineSetupRequest.md) |  | [default to undefined]
**coupons** | **Array&lt;any&gt;** | Discount coupon codes | [optional] [default to undefined]

## Example

```typescript
import { VPSV1VirtualMachinePurchaseRequest } from 'hostinger-api-sdk';

const instance: VPSV1VirtualMachinePurchaseRequest = {
    item_id,
    payment_method_id,
    setup,
    coupons,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
