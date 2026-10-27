# ReachV1WebsitesWebsiteResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Pass this to the disconnect endpoint matching &#x60;platform_type&#x60;. | [optional] [default to undefined]
**platform_type** | **string** | &#x60;wordpress&#x60;, &#x60;website_builder&#x60; (AI Website Builder site built manually) or &#x60;horizons&#x60; (site built with the agentic AI Website Builder). | [optional] [default to undefined]

## Example

```typescript
import { ReachV1WebsitesWebsiteResource } from '@hostinger/sdk';

const instance: ReachV1WebsitesWebsiteResource = {
    domain,
    platform_type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
