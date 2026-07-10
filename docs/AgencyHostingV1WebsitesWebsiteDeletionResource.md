# AgencyHostingV1WebsitesWebsiteDeletionResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_uid** | **string** | Deleted website UID | [optional] [default to undefined]
**status** | **string** | Deletion status | [optional] [default to undefined]
**message** | **string** | Human-readable result message | [optional] [default to undefined]
**deleted_at** | **string** |  | [optional] [default to undefined]
**is_cleanup_scheduled** | **boolean** | Whether background cleanup has been scheduled | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesWebsiteDeletionResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesWebsiteDeletionResource = {
    website_uid,
    status,
    message,
    deleted_at,
    is_cleanup_scheduled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
