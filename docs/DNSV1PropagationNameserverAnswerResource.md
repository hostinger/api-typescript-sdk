# DNSV1PropagationNameserverAnswerResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**nameserver** | **string** | Authoritative nameserver | [optional] [default to undefined]
**records** | **Array&lt;string&gt;** | Records the nameserver serves; null or empty when it serves none | [optional] [default to undefined]
**ttl** | **number** | TTL in seconds: how long resolvers may keep serving a previously cached value | [optional] [default to undefined]

## Example

```typescript
import { DNSV1PropagationNameserverAnswerResource } from '@hostinger/sdk';

const instance: DNSV1PropagationNameserverAnswerResource = {
    nameserver,
    records,
    ttl,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
