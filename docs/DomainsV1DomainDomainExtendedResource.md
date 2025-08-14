# DomainsV1DomainDomainExtendedResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name | [optional] [default to undefined]
**status** | **string** | Status of the domain | [optional] [default to undefined]
**message** | **string** |  | [optional] [default to undefined]
**is_privacy_protection_allowed** | **boolean** | Is privacy protection allowed for the domain | [optional] [default to undefined]
**is_privacy_protected** | **boolean** | Is privacy protection enabled for the domain | [optional] [default to undefined]
**is_lockable** | **boolean** | Is domain allowed to be locked | [optional] [default to undefined]
**is_locked** | **boolean** | Is domain locked | [optional] [default to undefined]
**name_servers** | [**DomainsV1DomainDomainExtendedResourceNameServers**](DomainsV1DomainDomainExtendedResourceNameServers.md) |  | [optional] [default to undefined]
**child_name_servers** | **Array&lt;Array&lt;string&gt;&gt;** | Child name servers | [optional] [default to undefined]
**domain_contacts** | [**DomainsV1DomainDomainExtendedResourceDomainContacts**](DomainsV1DomainDomainExtendedResourceDomainContacts.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]
**_60_days_lock_expires_at** | **string** |  | [optional] [default to undefined]
**registered_at** | **string** |  | [optional] [default to undefined]
**expires_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1DomainDomainExtendedResource } from 'hostinger-api-sdk';

const instance: DomainsV1DomainDomainExtendedResource = {
    domain,
    status,
    message,
    is_privacy_protection_allowed,
    is_privacy_protected,
    is_lockable,
    is_locked,
    name_servers,
    child_name_servers,
    domain_contacts,
    created_at,
    updated_at,
    _60_days_lock_expires_at,
    registered_at,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
