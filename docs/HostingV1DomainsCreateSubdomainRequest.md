# HostingV1DomainsCreateSubdomainRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subdomain** | **string** | Subdomain prefix to create under the selected website | [default to undefined]
**directory** | **string** | Directory name for the subdomain relative to the website root | [optional] [default to undefined]
**is_using_public_directory** | **boolean** | Use the website public directory as the subdomain root directory | [optional] [default to undefined]

## Example

```typescript
import { HostingV1DomainsCreateSubdomainRequest } from 'hostinger-api-sdk';

const instance: HostingV1DomainsCreateSubdomainRequest = {
    subdomain,
    directory,
    is_using_public_directory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
