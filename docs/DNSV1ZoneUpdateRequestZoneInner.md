# DNSV1ZoneUpdateRequestZoneInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the record (use &#x60;@&#x60; for wildcard name) | [default to undefined]
**records** | [**Array&lt;DNSV1ZoneUpdateRequestZoneInnerRecordsInner&gt;**](DNSV1ZoneUpdateRequestZoneInnerRecordsInner.md) | Records assigned to the name | [optional] [default to undefined]
**ttl** | **number** | TTL (Time-To-Live) of the record | [optional] [default to undefined]
**type** | **string** | Type of the record | [default to undefined]

## Example

```typescript
import { DNSV1ZoneUpdateRequestZoneInner } from 'hostinger-api-sdk';

const instance: DNSV1ZoneUpdateRequestZoneInner = {
    name,
    records,
    ttl,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
