# EcommerceV1PaymentProviderPaymentProviderListResourceDataConnectedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The store payment provider row ID. | [optional] [default to undefined]
**provider_id** | **string** | The payment gateway ID, e.g. stripe. | [optional] [default to undefined]
**title** | **string** | The provider title, or null. | [optional] [default to undefined]
**is_enabled** | **boolean** | Whether the provider is enabled for the store. | [optional] [default to undefined]
**status** | **string** | The connection status. | [optional] [default to undefined]
**shows_at_checkout** | **boolean** | Whether the provider shows at checkout. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1PaymentProviderPaymentProviderListResourceDataConnectedInner } from 'hostinger-api-sdk';

const instance: EcommerceV1PaymentProviderPaymentProviderListResourceDataConnectedInner = {
    id,
    provider_id,
    title,
    is_enabled,
    status,
    shows_at_checkout,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
