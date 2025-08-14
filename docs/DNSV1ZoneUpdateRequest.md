# DNSV1ZoneUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**overwrite** | **boolean** | If &#x60;true&#x60;, resource records (RRs) matching name and type will be deleted and new RRs will be created, otherwise resource records\&#39; ttl\&#39;s are updated and new records are appended. If no matching RRs are found, they are created. | [optional] [default to true]
**zone** | [**Array&lt;DNSV1ZoneUpdateRequestZoneInner&gt;**](DNSV1ZoneUpdateRequestZoneInner.md) |  | [default to undefined]

## Example

```typescript
import { DNSV1ZoneUpdateRequest } from 'hostinger-api-sdk';

const instance: DNSV1ZoneUpdateRequest = {
    overwrite,
    zone,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
