# ReachV1CampaignsCampaignDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**title** | **string** |  | [optional] [default to undefined]
**subject** | **string** |  | [optional] [default to undefined]
**sender_name** | **string** |  | [optional] [default to undefined]
**sender_email** | **string** |  | [optional] [default to undefined]
**template_uuid** | **string** | The email template this campaign uses. The template title is not exposed. | [optional] [default to undefined]
**status** | **string** | A fully sent campaign is &#x60;publish&#x60;. There is no &#x60;sent&#x60;, &#x60;paused&#x60; or &#x60;archived&#x60; status. | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**failure_reason** | **string** | Set only while the status is &#x60;failed&#x60;. | [optional] [default to undefined]
**is_smart_send** | **boolean** | Whether delivery time is picked per contact rather than sent to everyone at once. | [optional] [default to undefined]
**is_all_contacts** | **boolean** | Whether the campaign targets every contact instead of the listed segments. | [optional] [default to undefined]
**delivery** | [**ReachV1CampaignsCampaignDeliveryResource**](ReachV1CampaignsCampaignDeliveryResource.md) |  | [optional] [default to undefined]
**segment_uuids** | **Array&lt;string&gt;** | Segments this campaign targets. Empty when it targets all contacts. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]
**sent_at** | **string** |  | [optional] [default to undefined]
**scheduled_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsCampaignDetailsResource } from 'hostinger-api-sdk';

const instance: ReachV1CampaignsCampaignDetailsResource = {
    uuid,
    title,
    subject,
    sender_name,
    sender_email,
    template_uuid,
    status,
    type,
    failure_reason,
    is_smart_send,
    is_all_contacts,
    delivery,
    segment_uuids,
    created_at,
    updated_at,
    sent_at,
    scheduled_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
