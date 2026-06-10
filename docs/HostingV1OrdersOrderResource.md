# HostingV1OrdersOrderResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Order ID | [optional] [default to undefined]
**client_id** | **number** | Client ID | [optional] [default to undefined]
**subscription_id** | **string** | Subscription ID | [optional] [default to undefined]
**created_at** | **string** | Creation date | [optional] [default to undefined]
**plan** | [**HostingV1OrdersPlanResource**](HostingV1OrdersPlanResource.md) |  | [optional] [default to undefined]
**status** | **string** | Order status | [optional] [default to undefined]

## Example

```typescript
import { HostingV1OrdersOrderResource } from 'hostinger-api-sdk';

const instance: HostingV1OrdersOrderResource = {
    id,
    client_id,
    subscription_id,
    created_at,
    plan,
    status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
