# AgencyHostingV1WebsitesWebsiteListItemResourceDetails

Platform-specific website details. Shape depends on `platform`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uid** | **string** | Website UID | [optional] [default to undefined]
**ipv4** | **string** | IPv4 address | [optional] [default to undefined]
**flavor** | **string** | Setup flavor | [optional] [default to undefined]
**type** | **string** | Detected website type | [optional] [default to undefined]
**username** | **string** | Account username | [optional] [default to undefined]
**description** | **string** | Description | [optional] [default to undefined]
**state** | **string** | Application state | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**settings** | **object** | Website settings, e.g. PHP configuration | [optional] [default to undefined]
**wordpress** | **object** | WordPress installation details | [optional] [default to undefined]
**domains** | **Array&lt;object&gt;** | Application domains | [optional] [default to undefined]
**preview_domain** | **object** | Preview domain | [optional] [default to undefined]
**processes** | **Array&lt;object&gt;** | Ongoing website processes | [optional] [default to undefined]
**horizons_uuid** | **string** | Horizons UUID | [optional] [default to undefined]
**id** | **string** | Builder ID | [optional] [default to undefined]
**vhost** | **string** | Domain name | [optional] [default to undefined]
**uuid** | **string** | Application UUID | [optional] [default to undefined]
**title** | **string** | Application title | [optional] [default to undefined]
**port** | **number** | Application port | [optional] [default to undefined]
**runtime** | **string** | Application runtime | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesWebsiteListItemResourceDetails } from '@hostinger/sdk';

const instance: AgencyHostingV1WebsitesWebsiteListItemResourceDetails = {
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
    id,
    vhost,
    uuid,
    title,
    port,
    runtime,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
