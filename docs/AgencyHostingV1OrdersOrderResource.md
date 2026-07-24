# AgencyHostingV1OrdersOrderResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Order ID | [optional] [default to undefined]
**client_id** | **number** | Order client ID | [optional] [default to undefined]
**status** | **string** | Order status | [optional] [default to undefined]
**plan** | [**AgencyHostingV1OrdersPlanResource**](AgencyHostingV1OrdersPlanResource.md) |  | [optional] [default to undefined]
**datacenter** | [**AgencyHostingV1OrdersDatacenterResource**](AgencyHostingV1OrdersDatacenterResource.md) |  | [optional] [default to undefined]
**created_at** | **string** | Order creation date | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1OrdersOrderResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1OrdersOrderResource = {
    id,
    client_id,
    status,
    plan,
    datacenter,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
