# EcommerceV1VariantBatchUpdateVariantsRequestVariantsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**variant_id** | **string** | The id of the variant to update. | [default to undefined]
**title** | **string** | The variant title. | [optional] [default to undefined]
**inventory_quantity** | **number** | Units in stock. | [optional] [default to undefined]
**manage_inventory** | **boolean** | Whether stock is tracked for this variant. | [optional] [default to undefined]
**prices** | [**Array&lt;EcommerceV1VariantBatchUpdateVariantsRequestVariantsInnerPricesInner&gt;**](EcommerceV1VariantBatchUpdateVariantsRequestVariantsInnerPricesInner.md) | The full list of prices for the variant, replacing the existing ones. A free item is amount: 0. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1VariantBatchUpdateVariantsRequestVariantsInner } from '@hostinger/sdk';

const instance: EcommerceV1VariantBatchUpdateVariantsRequestVariantsInner = {
    variant_id,
    title,
    inventory_quantity,
    manage_inventory,
    prices,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
