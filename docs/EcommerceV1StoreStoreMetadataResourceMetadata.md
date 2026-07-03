# EcommerceV1StoreStoreMetadataResourceMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_payment_methods** | **boolean** | Whether the store has at least one payment method connected. | [optional] [default to undefined]
**has_shipping** | **boolean** | Whether the store has at least one shipping option configured. | [optional] [default to undefined]
**default_currency_code** | **string** | The default currency code of the store. | [optional] [default to undefined]
**default_currency** | [**EcommerceV1StoreStoreMetadataResourceMetadataDefaultCurrency**](EcommerceV1StoreStoreMetadataResourceMetadataDefaultCurrency.md) |  | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1StoreStoreMetadataResourceMetadata } from 'hostinger-api-sdk';

const instance: EcommerceV1StoreStoreMetadataResourceMetadata = {
    has_payment_methods,
    has_shipping,
    default_currency_code,
    default_currency,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
