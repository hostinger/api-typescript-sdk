# VPSV1DockerManagerContainerPortResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | Port mapping type - published (accessible from host), exposed (only internal), or range variants | [optional] [default to undefined]
**protocol** | **string** | Network protocol used for communication | [optional] [default to undefined]
**host_ip** | **string** | IP address on host where port is bound (null for exposed-only ports) | [optional] [default to undefined]
**host_port** | **number** | Port number on host machine (null for exposed-only or range ports) | [optional] [default to undefined]
**container_port** | **number** | Port number inside container (null for range ports) | [optional] [default to undefined]
**host_port_start** | **number** | Starting port number in host port range (null for single ports) | [optional] [default to undefined]
**host_port_end** | **number** | Ending port number in host port range (null for single ports) | [optional] [default to undefined]
**container_port_start** | **number** | Starting port number in container port range (null for single ports) | [optional] [default to undefined]
**container_port_end** | **number** | Ending port number in container port range (null for single ports) | [optional] [default to undefined]

## Example

```typescript
import { VPSV1DockerManagerContainerPortResource } from 'hostinger-api-sdk';

const instance: VPSV1DockerManagerContainerPortResource = {
    type,
    protocol,
    host_ip,
    host_port,
    container_port,
    host_port_start,
    host_port_end,
    container_port_start,
    container_port_end,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
