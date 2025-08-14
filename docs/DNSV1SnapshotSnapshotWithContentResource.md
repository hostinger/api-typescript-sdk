# DNSV1SnapshotSnapshotWithContentResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Snapshot ID | [optional] [default to undefined]
**reason** | **string** | Reason of the update | [optional] [default to undefined]
**snapshot** | [**Array&lt;DNSV1ZoneRecordResource&gt;**](DNSV1ZoneRecordResource.md) | Array of [&#x60;DNS.V1.Zone.RecordResource&#x60;](#model/dnsv1zonerecordresource) | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { DNSV1SnapshotSnapshotWithContentResource } from 'hostinger-api-sdk';

const instance: DNSV1SnapshotSnapshotWithContentResource = {
    id,
    reason,
    snapshot,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
