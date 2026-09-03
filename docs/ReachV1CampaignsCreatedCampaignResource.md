# ReachV1CampaignsCreatedCampaignResource

The campaign as it was stored, without targeting or delivery progress

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**title** | **string** |  | [optional] [default to undefined]
**subject** | **string** |  | [optional] [default to undefined]
**sender_name** | **string** |  | [optional] [default to undefined]
**sender_email** | **string** |  | [optional] [default to undefined]
**template_uuid** | **string** |  | [optional] [default to undefined]
**status** | **string** | Always &#x60;draft&#x60; for a campaign that was just created. | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**is_all_contacts** | **boolean** | Whether the campaign targets every contact instead of selected segments. | [optional] [default to undefined]
**metadata** | **{ [key: string]: string; }** | The stored extra fields, including the ones Reach sets itself. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsCreatedCampaignResource } from '@hostinger/sdk';

const instance: ReachV1CampaignsCreatedCampaignResource = {
    uuid,
    title,
    subject,
    sender_name,
    sender_email,
    template_uuid,
    status,
    type,
    is_all_contacts,
    metadata,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
