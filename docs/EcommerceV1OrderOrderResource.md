# EcommerceV1OrderOrderResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | The order ID, required by every other order endpoint. | [optional] [default to undefined]
**display_id** | **number** | The order number the merchant and customer see. | [optional] [default to undefined]
**status** | **string** | The order status. | [optional] [default to undefined]
**payment_status** | **string** | The payment status. A paid order is \&quot;captured\&quot;. | [optional] [default to undefined]
**fulfillment_status** | **string** | The fulfilment status. | [optional] [default to undefined]
**total** | **number** | Order total in the smallest currency unit. | [optional] [default to undefined]
**currency_code** | **string** | The order currency code. | [optional] [default to undefined]
**customer_email** | **string** | The customer email. | [optional] [default to undefined]
**item_count** | **number** | Number of distinct line items. Retrieve the order for the items themselves. | [optional] [default to undefined]
**created_at** | **string** | ISO timestamp of when the order was created. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1OrderOrderResource } from 'hostinger-api-sdk';

const instance: EcommerceV1OrderOrderResource = {
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
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
