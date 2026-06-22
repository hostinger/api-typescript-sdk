# EcommerceV1ProductCreateDigitalProductRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | The product name. | [default to undefined]
**price** | **number** | Price in the smallest currency unit (e.g. cents). Must be positive. | [default to undefined]
**description** | **string** | The product description. | [optional] [default to undefined]
**currency** | **string** | ISO 4217 currency code. Defaults to the store\&#39;s default currency when omitted. | [optional] [default to undefined]
**download_url** | **string** | Optional external download link delivered to the customer after purchase. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductCreateDigitalProductRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1ProductCreateDigitalProductRequest = {
    name,
    price,
    description,
    currency,
    download_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
