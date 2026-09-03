# ReachV1CampaignsStoreRequest

Create a campaign in draft status

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sender_name** | **string** | From name shown to the recipients. | [default to undefined]
**sender_email** | **string** | From address of the campaign. Its domain has to be verified on the profile before the campaign can be sent. | [default to undefined]
**title** | **string** | Name the campaign is listed under. Not shown to the recipients. | [optional] [default to undefined]
**subject** | **string** | Subject line of the email. | [optional] [default to undefined]
**template_uuid** | **string** | Template to send, as returned by the template endpoints. Can be left out and attached later, but the campaign cannot be sent without one. | [optional] [default to undefined]
**metadata** | [**ReachV1CampaignsStoreRequestMetadata**](ReachV1CampaignsStoreRequestMetadata.md) |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsStoreRequest } from '@hostinger/sdk';

const instance: ReachV1CampaignsStoreRequest = {
    sender_name,
    sender_email,
    title,
    subject,
    template_uuid,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
