# AgencyHostingV1WebsitesH5gWebsiteDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uid** | **string** | Website UID | [optional] [default to undefined]
**ipv4** | **string** | IPv4 address | [optional] [default to undefined]
**flavor** | **string** | Setup flavor | [optional] [default to undefined]
**type** | **string** | Detected website type | [optional] [default to undefined]
**username** | **string** | Username for this order | [optional] [default to undefined]
**description** | **string** | Description | [optional] [default to undefined]
**state** | **string** | Website state | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**settings** | **object** | Website settings, e.g. PHP configuration | [optional] [default to undefined]
**wordpress** | **object** | WordPress installation details | [optional] [default to undefined]
**domains** | **Array&lt;object&gt;** | Website domains | [optional] [default to undefined]
**preview_domain** | **object** | Preview domain | [optional] [default to undefined]
**processes** | **Array&lt;object&gt;** | Ongoing website processes | [optional] [default to undefined]
**horizons_uuid** | **string** | Horizons UUID (only for horizons websites) | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesH5gWebsiteDetailsResource } from '@hostinger/sdk';

const instance: AgencyHostingV1WebsitesH5gWebsiteDetailsResource = {
    uid,
    ipv4,
    flavor,
    type,
    username,
    description,
    state,
    created_at,
    settings,
    wordpress,
    domains,
    preview_domain,
    processes,
    horizons_uuid,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
