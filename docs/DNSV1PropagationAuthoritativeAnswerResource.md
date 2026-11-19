# DNSV1PropagationAuthoritativeAnswerResource

What the authoritative nameservers serve now: the best signal of the current record value

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**zone** | **string** | DNS zone that holds the record | [optional] [default to undefined]
**nameservers** | [**Array&lt;DNSV1PropagationNameserverAnswerResource&gt;**](DNSV1PropagationNameserverAnswerResource.md) | Answer of each authoritative nameserver of the zone | [optional] [default to undefined]

## Example

```typescript
import { DNSV1PropagationAuthoritativeAnswerResource } from '@hostinger/sdk';

const instance: DNSV1PropagationAuthoritativeAnswerResource = {
    zone,
    nameservers,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
