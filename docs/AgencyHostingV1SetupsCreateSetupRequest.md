# AgencyHostingV1SetupsCreateSetupRequest

Create a new Agency Plan website setup on the given order

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**datacenter_code** | **string** | Datacenter code where the website should be provisioned. Available codes depend on live capacity and are not a fixed set. | [default to undefined]
**flavor** | **string** | Setup flavor: a specific WordPress version in the format &#x60;wp-&lt;major&gt;.&lt;minor&gt;&#x60; or &#x60;wp-&lt;major&gt;.&lt;minor&gt;.&lt;patch&gt;&#x60; (e.g. &#x60;wp-6.8.2&#x60;), or &#x60;php-fpm&#x60; for a plain PHP stack. Generic versions like &#x60;wp-latest&#x60; are not allowed. | [default to undefined]
**settings** | [**AgencyHostingV1SetupsCreateSetupRequestSettings**](AgencyHostingV1SetupsCreateSetupRequestSettings.md) |  | [default to undefined]
**domain** | **string** | Primary domain to attach to the website. Omit or set to null to get a free auto-generated *.hostingersite.com subdomain instead. | [optional] [default to undefined]
**type** | **string** | Website type | [optional] [default to undefined]
**wordpress** | [**AgencyHostingV1SetupsCreateSetupRequestWordpress**](AgencyHostingV1SetupsCreateSetupRequestWordpress.md) |  | [optional] [default to undefined]
**clone** | [**AgencyHostingV1SetupsCreateSetupRequestClone**](AgencyHostingV1SetupsCreateSetupRequestClone.md) |  | [optional] [default to undefined]
**derive_domain** | [**AgencyHostingV1SetupsCreateSetupRequestDeriveDomain**](AgencyHostingV1SetupsCreateSetupRequestDeriveDomain.md) |  | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1SetupsCreateSetupRequest } from 'hostinger-api-sdk';

const instance: AgencyHostingV1SetupsCreateSetupRequest = {
    datacenter_code,
    flavor,
    settings,
    domain,
    type,
    wordpress,
    clone,
    derive_domain,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
