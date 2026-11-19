# DNSV1PropagationVantagePointResource

Answer of a public resolver at one location

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | **string** | Country code of the resolver | [optional] [default to undefined]
**provider** | **string** | Resolver provider | [optional] [default to undefined]
**ip** | **string** | IP address of the resolver | [optional] [default to undefined]
**location** | **string** | Location of the resolver | [optional] [default to undefined]
**latitude** | **number** |  | [optional] [default to undefined]
**longitude** | **number** |  | [optional] [default to undefined]
**records** | **Array&lt;string&gt;** | Records the resolver returned; null when it returned none or could not be queried | [optional] [default to undefined]
**is_propagated** | **boolean** | Whether this location returns the same records as the authoritative nameservers. For GeoDNS domains, whose nameservers answer differently by region, true means the location returned a record. A records served from the Hostinger CDN count as propagated when the location also returns CDN addresses. True when every responding authoritative nameserver returns no records. Null when the location could not be queried or no authoritative answer could be compared. | [optional] [default to undefined]

## Example

```typescript
import { DNSV1PropagationVantagePointResource } from '@hostinger/sdk';

const instance: DNSV1PropagationVantagePointResource = {
    country,
    provider,
    ip,
    location,
    latitude,
    longitude,
    records,
    is_propagated,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
