# EcommerceV1PaymentProviderPaymentProviderListResourceDataAvailableInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The payment gateway ID, e.g. stripe. | [optional] [default to undefined]
**is_installed** | **boolean** | Whether the gateway is installed on the store. | [optional] [default to undefined]
**is_enabled** | **boolean** | Whether the gateway is enabled on the store. | [optional] [default to undefined]
**is_currency_supported** | **boolean** | Whether the gateway supports the store currency. | [optional] [default to undefined]
**supported_currencies** | **Array&lt;string&gt;** | Currencies the gateway supports; present only when the store currency is unsupported. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1PaymentProviderPaymentProviderListResourceDataAvailableInner } from 'hostinger-api-sdk';

const instance: EcommerceV1PaymentProviderPaymentProviderListResourceDataAvailableInner = {
    id,
    is_installed,
    is_enabled,
    is_currency_supported,
    supported_currencies,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
