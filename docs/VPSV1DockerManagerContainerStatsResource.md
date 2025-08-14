# VPSV1DockerManagerContainerStatsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cpu_percentage** | **number** | CPU usage in percentage | [optional] [default to undefined]
**memory_percentage** | **number** | Memory usage in percentage | [optional] [default to undefined]
**memory_used** | **number** | Used memory in bytes | [optional] [default to undefined]
**memory_total** | **number** | Total available memory in bytes | [optional] [default to undefined]
**net_in** | **number** | Inbound network traffic in bytes | [optional] [default to undefined]
**net_out** | **number** | Outbound network traffic in bytes | [optional] [default to undefined]

## Example

```typescript
import { VPSV1DockerManagerContainerStatsResource } from 'hostinger-api-sdk';

const instance: VPSV1DockerManagerContainerStatsResource = {
    cpu_percentage,
    memory_percentage,
    memory_used,
    memory_total,
    net_in,
    net_out,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
