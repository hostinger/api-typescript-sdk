# EcommerceV1OrderOrderDetailResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The order ID. | [optional] [default to undefined]
**display_id** | **number** | The order number. | [optional] [default to undefined]
**status** | **string** | The order status. | [optional] [default to undefined]
**payment_status** | **string** | The payment status. | [optional] [default to undefined]
**fulfillment_status** | **string** | The fulfilment status. | [optional] [default to undefined]
**total** | **number** | Order total in the smallest currency unit. | [optional] [default to undefined]
**currency_code** | **string** | The order currency code. | [optional] [default to undefined]
**customer_email** | **string** | The customer email. | [optional] [default to undefined]
**item_count** | **number** | Number of distinct line items. | [optional] [default to undefined]
**created_at** | **string** | ISO timestamp of when the order was created. | [optional] [default to undefined]
**merchant_note** | **string** | Internal note visible only to the merchant. | [optional] [default to undefined]
**subtotal** | **number** | Subtotal in the smallest currency unit. | [optional] [default to undefined]
**discount_total** | **number** | Discount total in the smallest currency unit. | [optional] [default to undefined]
**tax_total** | **number** | Tax total in the smallest currency unit. | [optional] [default to undefined]
**shipping_total** | **number** | Shipping total in the smallest currency unit. | [optional] [default to undefined]
**paid_total** | **number** | Amount paid in the smallest currency unit. | [optional] [default to undefined]
**refunded_total** | **number** | Amount refunded in the smallest currency unit. | [optional] [default to undefined]
**shipping_address** | [**EcommerceV1OrderOrderDetailResourceShippingAddress**](EcommerceV1OrderOrderDetailResourceShippingAddress.md) |  | [optional] [default to undefined]
**billing_address** | [**EcommerceV1OrderOrderDetailResourceBillingAddress**](EcommerceV1OrderOrderDetailResourceBillingAddress.md) |  | [optional] [default to undefined]
**items** | [**Array&lt;EcommerceV1OrderOrderDetailResourceItemsInner&gt;**](EcommerceV1OrderOrderDetailResourceItemsInner.md) | The order line items. | [optional] [default to undefined]
**fulfillments** | [**Array&lt;EcommerceV1OrderOrderDetailResourceFulfillmentsInner&gt;**](EcommerceV1OrderOrderDetailResourceFulfillmentsInner.md) | The order fulfilments with tracking. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1OrderOrderDetailResource } from '@hostinger/sdk';

const instance: EcommerceV1OrderOrderDetailResource = {
    id,
    display_id,
    status,
    payment_status,
    fulfillment_status,
    total,
    currency_code,
    customer_email,
    item_count,
    created_at,
    merchant_note,
    subtotal,
    discount_total,
    tax_total,
    shipping_total,
    paid_total,
    refunded_total,
    shipping_address,
    billing_address,
    items,
    fulfillments,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
