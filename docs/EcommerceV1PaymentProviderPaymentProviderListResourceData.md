# EcommerceV1PaymentProviderPaymentProviderListResourceData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connected** | [**Array&lt;EcommerceV1PaymentProviderPaymentProviderListResourceDataConnectedInner&gt;**](EcommerceV1PaymentProviderPaymentProviderListResourceDataConnectedInner.md) | Payment providers already connected to the store. | [optional] [default to undefined]
**available** | [**Array&lt;EcommerceV1PaymentProviderPaymentProviderListResourceDataAvailableInner&gt;**](EcommerceV1PaymentProviderPaymentProviderListResourceDataAvailableInner.md) | Payment gateways available to install for the store. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1PaymentProviderPaymentProviderListResourceData } from 'hostinger-api-sdk';

const instance: EcommerceV1PaymentProviderPaymentProviderListResourceData = {
    connected,
    available,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
