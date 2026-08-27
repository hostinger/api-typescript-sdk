# EcommerceV1VariantCreateVariantRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | The variant title. Defaults to the option values joined with \&#39; / \&#39; (e.g. \&#39;Red / L\&#39;). | [optional] [default to undefined]
**sku** | **string** | The variant SKU. | [optional] [default to undefined]
**_options** | [**Array&lt;EcommerceV1VariantCreateVariantRequestOptionsInner&gt;**](EcommerceV1VariantCreateVariantRequestOptionsInner.md) | Option name/value pairs that distinguish this variant, e.g. [{name: Size, value: M}]. Options missing from the product are created; provide a value for every option the product already has. | [default to undefined]
**prices** | [**Array&lt;EcommerceV1VariantCreateVariantRequestPricesInner&gt;**](EcommerceV1VariantCreateVariantRequestPricesInner.md) | Prices per currency. Amounts are integers in the smallest currency unit. A free item is amount: 0. | [optional] [default to undefined]
**inventory_quantity** | **number** | Units in stock. Defaults to 0. | [optional] [default to undefined]
**manage_inventory** | **boolean** | Whether stock is tracked for this variant. Defaults to false. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1VariantCreateVariantRequest } from '@hostinger/sdk';

const instance: EcommerceV1VariantCreateVariantRequest = {
    title,
    sku,
    _options,
    prices,
    inventory_quantity,
    manage_inventory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
