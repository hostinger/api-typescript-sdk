# EcommerceV1DiscountCreateDiscountRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **string** | The discount code customers enter at checkout. | [default to undefined]
**name** | **string** | A human-friendly discount name. | [optional] [default to undefined]
**type** | **string** | The discount type. | [default to undefined]
**value** | **number** | For percentage discounts a whole number 1-100; for fixed discounts an amount in the smallest currency unit (e.g. $10 is 1000). Ignored for free_shipping. | [default to undefined]
**allocation** | **string** | Whether the discount applies to the cart total or to each eligible item. | [optional] [default to undefined]
**starts_at** | **string** | When the discount becomes active. A bare date (2026-11-27) anchors to time_zone. Defaults to now when omitted. | [optional] [default to undefined]
**ends_at** | **string** | When the discount expires. A bare date runs to the end of that day in time_zone. Never expires when omitted. | [optional] [default to undefined]
**usage_limit** | **number** | Maximum number of times the discount can be redeemed. | [optional] [default to undefined]
**min_cart_value** | **number** | Minimum cart value in the smallest currency unit required for the discount to apply. | [optional] [default to undefined]
**time_zone** | **string** | IANA time zone used to interpret starts_at and ends_at. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1DiscountCreateDiscountRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1DiscountCreateDiscountRequest = {
    code,
    name,
    type,
    value,
    allocation,
    starts_at,
    ends_at,
    usage_limit,
    min_cart_value,
    time_zone,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
