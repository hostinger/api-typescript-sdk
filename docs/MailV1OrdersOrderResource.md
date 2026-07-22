# MailV1OrdersOrderResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Order resource ID | [optional] [default to undefined]
**status** | **string** | Order status | [optional] [default to undefined]
**is_trial** | **boolean** | Whether the order is currently in a trial period | [optional] [default to undefined]
**seats** | **number** | Number of mailbox seats purchased with the order | [optional] [default to undefined]
**domain** | [**MailV1OrdersOrderDomainResource**](MailV1OrdersOrderDomainResource.md) |  | [optional] [default to undefined]
**plan** | [**MailV1OrdersOrderPlanResource**](MailV1OrdersOrderPlanResource.md) |  | [optional] [default to undefined]
**has_pending_upgrade** | **boolean** | Whether an upgrade is currently pending for the order | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**expires_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1OrdersOrderResource } from 'hostinger-api-sdk';

const instance: MailV1OrdersOrderResource = {
    id,
    status,
    is_trial,
    seats,
    domain,
    plan,
    has_pending_upgrade,
    created_at,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
