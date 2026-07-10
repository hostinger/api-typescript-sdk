# AgencyHostingV1WebsitesWebsiteDomainDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fqdn** | **string** | Domain name | [optional] [default to undefined]
**parent_fqdn** | **string** | Parent domain name if the domain is a subdomain | [optional] [default to undefined]
**ipv6** | **string** | IPv6 address | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**nameservers** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**ssl_cert** | [**AgencyHostingV1WebsitesSslCertResource**](AgencyHostingV1WebsitesSslCertResource.md) |  | [optional] [default to undefined]
**custom_ssl_cert** | [**AgencyHostingV1WebsitesCustomSslCertResource**](AgencyHostingV1WebsitesCustomSslCertResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesWebsiteDomainDetailsResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesWebsiteDomainDetailsResource = {
    fqdn,
    parent_fqdn,
    ipv6,
    created_at,
    nameservers,
    ssl_cert,
    custom_ssl_cert,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
