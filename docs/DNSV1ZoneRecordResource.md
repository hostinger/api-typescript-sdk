# DNSV1ZoneRecordResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of the record (use &#x60;@&#x60; for wildcard name) | [optional] [default to undefined]
**records** | [**Array&lt;DNSV1ZoneNameRecordResource&gt;**](DNSV1ZoneNameRecordResource.md) | Array of [&#x60;DNS.V1.Zone.NameRecordResource&#x60;](#model/dnsv1zonenamerecordresource) | [optional] [default to undefined]
**ttl** | **number** | TTL (Time-To-Live) of the record | [optional] [default to undefined]
**type** | **string** | Type of the record | [optional] [default to undefined]

## Example

```typescript
import { DNSV1ZoneRecordResource } from 'hostinger-api-sdk';

const instance: DNSV1ZoneRecordResource = {
    name,
    records,
    ttl,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
