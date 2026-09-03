# ReachV1CampaignsStoreRequestMetadata

Extra campaign fields. Any key outside the listed ones is rejected.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**preheader** | **string** | Preview text shown after the subject line in the inbox. | [optional] [default to undefined]
**source** | **string** | Where the campaign was created from. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1CampaignsStoreRequestMetadata } from '@hostinger/sdk';

const instance: ReachV1CampaignsStoreRequestMetadata = {
    preheader,
    source,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
