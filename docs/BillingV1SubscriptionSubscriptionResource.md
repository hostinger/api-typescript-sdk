# BillingV1SubscriptionSubscriptionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Subscription ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**billing_period** | **number** |  | [optional] [default to undefined]
**billing_period_unit** | **string** |  | [optional] [default to undefined]
**currency_code** | **string** |  | [optional] [default to undefined]
**total_price** | **number** | Total price in cents | [optional] [default to undefined]
**renewal_price** | **number** | Renewal price in cents | [optional] [default to undefined]
**is_auto_renewed** | **boolean** |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**expires_at** | **string** |  | [optional] [default to undefined]
**next_billing_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { BillingV1SubscriptionSubscriptionResource } from 'hostinger-api-sdk';

const instance: BillingV1SubscriptionSubscriptionResource = {
    id,
    name,
    status,
    billing_period,
    billing_period_unit,
    currency_code,
    total_price,
    renewal_price,
    is_auto_renewed,
    created_at,
    expires_at,
    next_billing_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
