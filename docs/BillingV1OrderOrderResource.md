# BillingV1OrderOrderResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Order ID | [optional] [default to undefined]
**subscription_id** | **string** | Subscription ID | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**currency** | **string** | Currency code | [optional] [default to undefined]
**subtotal** | **number** | Subtotal price (exc. VAT) in cents | [optional] [default to undefined]
**total** | **number** | Total price (inc. VAT) in cents | [optional] [default to undefined]
**billing_address** | [**BillingV1OrderOrderBillingAddressResource**](BillingV1OrderOrderBillingAddressResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { BillingV1OrderOrderResource } from 'hostinger-api-sdk';

const instance: BillingV1OrderOrderResource = {
    id,
    subscription_id,
    status,
    currency,
    subtotal,
    total,
    billing_address,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
