# HorizonsV1WebsitesPublishedWebsiteResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | Always &#x60;publishing&#x60; - the build runs asynchronously after this response | [default to undefined]
**published_url** | **string** | The URL the published website will be live on in a few minutes | [default to undefined]
**website_url** | **string** | The website URL for the user to track progress in Hostinger Horizons interface | [default to undefined]
**website_id** | **string** | The website ID | [default to undefined]

## Example

```typescript
import { HorizonsV1WebsitesPublishedWebsiteResource } from '@hostinger/sdk';

const instance: HorizonsV1WebsitesPublishedWebsiteResource = {
    status,
    published_url,
    website_url,
    website_id,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
