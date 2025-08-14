# VPSV1DockerManagerLogsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**service** | **string** | Name of the Docker Compose service that generated these log entries | [optional] [default to undefined]
**entries** | [**Array&lt;VPSV1DockerManagerLogEntryResource&gt;**](VPSV1DockerManagerLogEntryResource.md) | Array of [&#x60;VPS.V1.DockerManager.LogEntryResource&#x60;](#model/vpsv1dockermanagerlogentryresource) | [optional] [default to undefined]

## Example

```typescript
import { VPSV1DockerManagerLogsResource } from 'hostinger-api-sdk';

const instance: VPSV1DockerManagerLogsResource = {
    service,
    entries,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
