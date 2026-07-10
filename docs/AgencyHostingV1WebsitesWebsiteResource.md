# AgencyHostingV1WebsitesWebsiteResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uid** | **string** | Website UID | [optional] [default to undefined]
**ipv4** | **string** | IPv4 address | [optional] [default to undefined]
**flavor** | **string** | Setup flavor | [optional] [default to undefined]
**type** | **string** | Website type | [optional] [default to undefined]
**description** | **string** | Description | [optional] [default to undefined]
**state** | **string** | Website state | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**domains** | [**Array&lt;AgencyHostingV1WebsitesWebsiteDomainDetailsResource&gt;**](AgencyHostingV1WebsitesWebsiteDomainDetailsResource.md) | Array of [&#x60;AgencyHosting.V1.Websites.WebsiteDomainDetailsResource&#x60;](#model/agencyhostingv1websiteswebsitedomaindetailsresource) | [optional] [default to undefined]
**preview_domain** | [**AgencyHostingV1WebsitesWebsitePreviewDomainResource**](AgencyHostingV1WebsitesWebsitePreviewDomainResource.md) |  | [optional] [default to undefined]
**settings** | [**AgencyHostingV1WebsitesWebsiteSettingsResource**](AgencyHostingV1WebsitesWebsiteSettingsResource.md) |  | [optional] [default to undefined]
**wordpress** | [**AgencyHostingV1WebsitesWordPressInstallResource**](AgencyHostingV1WebsitesWordPressInstallResource.md) |  | [optional] [default to undefined]
**remote_access** | [**AgencyHostingV1WebsitesWebsiteRemoteAccessResource**](AgencyHostingV1WebsitesWebsiteRemoteAccessResource.md) |  | [optional] [default to undefined]
**server** | [**AgencyHostingV1WebsitesWebsiteServerResource**](AgencyHostingV1WebsitesWebsiteServerResource.md) |  | [optional] [default to undefined]
**order** | [**AgencyHostingV1WebsitesWebsiteOrderResource**](AgencyHostingV1WebsitesWebsiteOrderResource.md) |  | [optional] [default to undefined]
**user** | [**AgencyHostingV1WebsitesWebsiteUserResource**](AgencyHostingV1WebsitesWebsiteUserResource.md) |  | [optional] [default to undefined]
**staging_root** | [**AgencyHostingV1WebsitesWebsiteStagingRootResource**](AgencyHostingV1WebsitesWebsiteStagingRootResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesWebsiteResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesWebsiteResource = {
    uid,
    ipv4,
    flavor,
    type,
    description,
    state,
    created_at,
    domains,
    preview_domain,
    settings,
    wordpress,
    remote_access,
    server,
    order,
    user,
    staging_root,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
