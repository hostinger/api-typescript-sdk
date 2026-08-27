# EcommerceV1ProductProductResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The product ID, required by every other product endpoint. | [optional] [default to undefined]
**title** | **string** | The product name. | [optional] [default to undefined]
**status** | **string** | The product status. | [optional] [default to undefined]
**thumbnail** | **string** | The product\&#39;s primary image URL, or null. | [optional] [default to undefined]
**type** | **string** | The product type. | [optional] [default to undefined]
**variant_count** | **number** | Number of variants. Use include&#x3D;variants to retrieve them. | [optional] [default to undefined]
**price_range** | [**EcommerceV1ProductProductResourcePriceRange**](EcommerceV1ProductProductResourcePriceRange.md) |  | [optional] [default to undefined]
**variants** | [**Array&lt;EcommerceV1ProductProductResourceVariantsInner&gt;**](EcommerceV1ProductProductResourceVariantsInner.md) | Present (non-null) only when include&#x3D;variants is set; null otherwise. | [optional] [default to undefined]
**media** | [**Array&lt;EcommerceV1ProductProductResourceMediaInner&gt;**](EcommerceV1ProductProductResourceMediaInner.md) | Present (non-null) only when include&#x3D;media is set; null otherwise. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductProductResource } from '@hostinger/sdk';

const instance: EcommerceV1ProductProductResource = {
    id,
    title,
    status,
    thumbnail,
    type,
    variant_count,
    price_range,
    variants,
    media,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
