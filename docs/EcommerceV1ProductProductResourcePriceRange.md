# EcommerceV1ProductProductResourcePriceRange

Effective price bounds across the product\'s variants.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**min** | **number** | Lowest effective variant price in the smallest currency unit, or null if unpriced. | [optional] [default to undefined]
**max** | **number** | Highest effective variant price in the smallest currency unit, or null if unpriced. | [optional] [default to undefined]
**currency_code** | **string** | The store currency the range is expressed in. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductProductResourcePriceRange } from '@hostinger/sdk';

const instance: EcommerceV1ProductProductResourcePriceRange = {
    min,
    max,
    currency_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
