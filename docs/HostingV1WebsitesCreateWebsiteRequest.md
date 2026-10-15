# HostingV1WebsitesCreateWebsiteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name for the website. Cannot start with \&quot;www.\&quot; and can have at most one subdomain level, e.g. &#x60;blog.example.com&#x60;. | [default to undefined]
**order_id** | **number** | Hosting order ID to create this website on. Choose the order whose hosting plan should host the new website. List orders to find available IDs. | [default to undefined]
**datacenter_code** | **string** | Datacenter for the hosting account when the order does not have one yet. Omit to use the order\&#39;s default datacenter. Ignored when the order already has a hosting account. Must be an available datacenter; list available datacenters to find valid codes. | [optional] [default to undefined]

## Example

```typescript
import { HostingV1WebsitesCreateWebsiteRequest } from '@hostinger/sdk';

const instance: HostingV1WebsitesCreateWebsiteRequest = {
    domain,
    order_id,
    datacenter_code,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
