# HostingV1DomainsParkedDomainResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **string** | Website username | [optional] [default to undefined]
**domain** | **string** | Parked domain name or IP address | [optional] [default to undefined]
**parent_domain** | **string** | Parent website domain | [optional] [default to undefined]
**root_directory** | **string** | Parked domain root directory | [optional] [default to undefined]
**type** | **string** | Whether the parked value is a domain name or an IP address (IPv4 or IPv6) | [optional] [default to undefined]

## Example

```typescript
import { HostingV1DomainsParkedDomainResource } from 'hostinger-api-sdk';

const instance: HostingV1DomainsParkedDomainResource = {
    username,
    domain,
    parent_domain,
    root_directory,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
