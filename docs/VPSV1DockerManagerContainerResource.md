# VPSV1DockerManagerContainerResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique container identifier (short form of Docker container ID) | [optional] [default to undefined]
**name** | **string** | Container name as defined in docker-compose or assigned by Docker | [optional] [default to undefined]
**image** | **string** | Docker image name and tag used to create this container | [optional] [default to undefined]
**command** | **string** | Command being executed inside the container (may be truncated with ...) | [optional] [default to undefined]
**status** | **string** | Human-readable container status including uptime, exit codes, or error information | [optional] [default to undefined]
**state** | **string** | Programmatic container lifecycle state for automated processing | [optional] [default to undefined]
**health** | **string** | Container health status | [optional] [default to undefined]
**ports** | [**Array&lt;VPSV1DockerManagerContainerPortResource&gt;**](VPSV1DockerManagerContainerPortResource.md) | Array of [&#x60;VPS.V1.DockerManager.ContainerPortResource&#x60;](#model/vpsv1dockermanagercontainerportresource) | [optional] [default to undefined]
**stats** | [**VPSV1DockerManagerContainerStatsResource**](VPSV1DockerManagerContainerStatsResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { VPSV1DockerManagerContainerResource } from 'hostinger-api-sdk';

const instance: VPSV1DockerManagerContainerResource = {
    id,
    name,
    image,
    command,
    status,
    state,
    health,
    ports,
    stats,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
