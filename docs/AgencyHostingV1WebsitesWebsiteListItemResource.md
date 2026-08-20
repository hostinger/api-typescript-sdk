# AgencyHostingV1WebsitesWebsiteListItemResource

Website item. The `details` shape differs per platform — see the `platform` field.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**client_id** | **number** |  | [default to undefined]
**order_id** | **number** |  | [default to undefined]
**platform** | **string** | Website platform | [default to undefined]
**state** | **string** | Website state | [default to undefined]
**created_at** | **string** |  | [default to undefined]
**plan** | [**AgencyHostingV1WebsitesPlanResource**](AgencyHostingV1WebsitesPlanResource.md) |  | [default to undefined]
**details** | [**AgencyHostingV1WebsitesWebsiteListItemResourceDetails**](AgencyHostingV1WebsitesWebsiteListItemResourceDetails.md) |  | [default to undefined]
**suspension_reason** | **string** | Reason for suspension, only populated for payment related suspensions | [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesWebsiteListItemResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesWebsiteListItemResource = {
    id,
    client_id,
    order_id,
    platform,
    state,
    created_at,
    plan,
    details,
    suspension_reason,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
