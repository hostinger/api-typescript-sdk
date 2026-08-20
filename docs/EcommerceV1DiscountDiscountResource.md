# EcommerceV1DiscountDiscountResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The discount ID, required by every other discount endpoint. | [optional] [default to undefined]
**code** | **string** | The discount code customers enter at checkout. | [optional] [default to undefined]
**name** | **string** | The discount name, or null. | [optional] [default to undefined]
**type** | **string** | The discount type, or null. | [optional] [default to undefined]
**value** | **number** | The discount value, or null. Percentage is 1-100; fixed is in the smallest currency unit. | [optional] [default to undefined]
**allocation** | **string** | Whether the discount applies to the cart total or to each item, or null. | [optional] [default to undefined]
**is_disabled** | **boolean** | Whether the discount is disabled. | [optional] [default to undefined]
**starts_at** | **string** | When the discount becomes active. | [optional] [default to undefined]
**ends_at** | **string** | When the discount expires, or null. | [optional] [default to undefined]
**usage_limit** | **number** | Maximum number of redemptions, or null for unlimited. | [optional] [default to undefined]
**usage_count** | **number** | Number of times the discount has been redeemed. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1DiscountDiscountResource } from 'hostinger-api-sdk';

const instance: EcommerceV1DiscountDiscountResource = {
    id,
    code,
    name,
    type,
    value,
    allocation,
    is_disabled,
    starts_at,
    ends_at,
    usage_limit,
    usage_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
