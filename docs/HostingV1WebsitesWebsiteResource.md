# HostingV1WebsitesWebsiteResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Website domain. Null for U4S websites with no domain attached. | [optional] [default to undefined]
**vhost_type** | **string** | Virtual host type. Only present for CloudLinux websites. | [optional] [default to undefined]
**is_enabled** | **boolean** | Whether website is enabled | [optional] [default to undefined]
**username** | **string** | Username. Not applicable for U4S websites. | [optional] [default to undefined]
**client_id** | **number** | Client ID | [optional] [default to undefined]
**order_id** | **number** | Order ID | [optional] [default to undefined]
**created_at** | **string** | Creation date | [optional] [default to undefined]
**root_directory** | **string** | Root directory path. Only present for CloudLinux websites. | [optional] [default to undefined]
**parent_domain** | **string** | Parent domain | [optional] [default to undefined]
**website_type** | **string** | Type of website detected on the underlying platform. | [optional] [default to undefined]
**horizons_uuid** | **string** | Horizons UUID. Only present for horizons websites. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1WebsitesWebsiteResource } from '@hostinger/sdk';

const instance: HostingV1WebsitesWebsiteResource = {
    domain,
    vhost_type,
    is_enabled,
    username,
    client_id,
    order_id,
    created_at,
    root_directory,
    parent_domain,
    website_type,
    horizons_uuid,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
