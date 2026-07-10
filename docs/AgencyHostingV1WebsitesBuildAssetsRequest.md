# AgencyHostingV1WebsitesBuildAssetsRequest

Build Node.js assets from an already-uploaded archive

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**archive_path** | **string** | Directory, relative to the website document root, where the uploaded site archive currently lives. Most commonly this is simply &#x60;public_html&#x60;. | [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesBuildAssetsRequest } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesBuildAssetsRequest = {
    archive_path,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
