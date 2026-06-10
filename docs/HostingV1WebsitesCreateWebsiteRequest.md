# HostingV1WebsitesCreateWebsiteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name for the website. Cannot start with \&quot;www.\&quot; | [default to undefined]
**order_id** | **number** | ID of the associated order | [default to undefined]
**datacenter_code** | **string** | Datacenter code. This parameter is required when creating the first website on a new hosting plan. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1WebsitesCreateWebsiteRequest } from 'hostinger-api-sdk';

const instance: HostingV1WebsitesCreateWebsiteRequest = {
    domain,
    order_id,
    datacenter_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
