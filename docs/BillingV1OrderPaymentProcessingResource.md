# BillingV1OrderPaymentProcessingResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Order ID | [optional] [default to undefined]
**subscription_id** | **string** | Subscription ID, use it to find the product once the order completes | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**message** | **string** | Explanation of what happens next | [optional] [default to undefined]

## Example

```typescript
import { BillingV1OrderPaymentProcessingResource } from '@hostinger/sdk';

const instance: BillingV1OrderPaymentProcessingResource = {
    id,
    subscription_id,
    status,
    message,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
