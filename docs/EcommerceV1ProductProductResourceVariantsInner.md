# EcommerceV1ProductProductResourceVariantsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The variant ID. | [optional] [default to undefined]
**title** | **string** | The variant title. | [optional] [default to undefined]
**sku** | **string** | The variant SKU. | [optional] [default to undefined]
**_options** | [**Array&lt;EcommerceV1ProductProductResourceVariantsInnerOptionsInner&gt;**](EcommerceV1ProductProductResourceVariantsInnerOptionsInner.md) | The variant\&#39;s option values. | [optional] [default to undefined]
**prices** | [**Array&lt;EcommerceV1ProductProductResourceVariantsInnerPricesInner&gt;**](EcommerceV1ProductProductResourceVariantsInnerPricesInner.md) | Prices per currency, in the smallest currency unit. | [optional] [default to undefined]
**inventory_quantity** | **number** | Units in stock. | [optional] [default to undefined]
**manage_inventory** | **boolean** | Whether stock is tracked for this variant. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductProductResourceVariantsInner } from 'hostinger-api-sdk';

const instance: EcommerceV1ProductProductResourceVariantsInner = {
    id,
    title,
    sku,
    _options,
    prices,
    inventory_quantity,
    manage_inventory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
