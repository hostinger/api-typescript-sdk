# EcommerceV1VariantBatchUpdateVariantsRequestVariantsInnerPricesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | **number** | Price in the smallest currency unit (e.g. cents). | [default to undefined]
**sale_amount** | **number** | Optional sale price in the smallest currency unit; must be lower than amount. | [optional] [default to undefined]
**currency** | **string** | ISO 4217 currency code. Defaults to the store\&#39;s default currency. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1VariantBatchUpdateVariantsRequestVariantsInnerPricesInner } from 'hostinger-api-sdk';

const instance: EcommerceV1VariantBatchUpdateVariantsRequestVariantsInnerPricesInner = {
    amount,
    sale_amount,
    currency,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
