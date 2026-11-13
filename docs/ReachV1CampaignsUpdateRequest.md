# ReachV1CampaignsUpdateRequest

Update a campaign. Send at least one field; fields left out keep their current value.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Name the campaign is listed under. Not shown to the recipients. | [optional] [default to undefined]
**subject** | **string** | Subject line of the email. | [optional] [default to undefined]
**sender_name** | **string** | From name shown to the recipients. | [optional] [default to undefined]
**sender_email** | **string** | From address of the campaign. Its domain has to be verified on the profile before the campaign can be sent. | [optional] [default to undefined]
**template_uuid** | **string** | Template to send, as returned by the template endpoints. | [optional] [default to undefined]
**all_contacts** | **boolean** | &#x60;true&#x60; targets every contact of the profile, &#x60;false&#x60; targets only &#x60;segment_uuids&#x60;. Required when &#x60;segment_uuids&#x60; or &#x60;excluded_segment_uuids&#x60; is sent. | [optional] [default to undefined]
**segment_uuids** | **Array&lt;string&gt;** | Segments to target. Replaces the segments currently targeted. | [optional] [default to undefined]
**excluded_segment_uuids** | **Array&lt;string&gt;** | Segments to leave out. Only allowed together with &#x60;all_contacts: true&#x60;. | [optional] [default to undefined]
**metadata** | [**ReachV1CampaignsStoreRequestMetadata**](ReachV1CampaignsStoreRequestMetadata.md) |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsUpdateRequest } from '@hostinger/sdk';

const instance: ReachV1CampaignsUpdateRequest = {
    title,
    subject,
    sender_name,
    sender_email,
    template_uuid,
    all_contacts,
    segment_uuids,
    excluded_segment_uuids,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
