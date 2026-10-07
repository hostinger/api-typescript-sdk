# HorizonsV1WebsitesWebsiteUrlResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_url** | **string** | The website URL for the user to access their website in Hostinger Horizons interface | [default to undefined]
**published_at** | **string** | When the website was last published, or null if it has never been published | [optional] [default to undefined]
**is_template** | **boolean** | Whether the website is published as a template, so its published pages show a \&quot;Use template\&quot; banner | [optional] [default to undefined]
**is_in_progress** | **boolean** | Whether Hostinger Horizons is still generating changes or publishing the website. Publishing is refused while it is true, and editing while changes are being generated. An unfinished template migration also refuses publishing, with its own error, without setting this flag. | [optional] [default to undefined]
**has_ecommerce_store** | **boolean** | Whether the website has an ecommerce store | [optional] [default to undefined]

## Example

```typescript
import { HorizonsV1WebsitesWebsiteUrlResource } from '@hostinger/sdk';

const instance: HorizonsV1WebsitesWebsiteUrlResource = {
    website_url,
    published_at,
    is_template,
    is_in_progress,
    has_ecommerce_store,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
