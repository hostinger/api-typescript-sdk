# VPSV1DockerManagerProjectResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Docker Compose project name (derived from directory name or compose file) | [optional] [default to undefined]
**status** | **string** | Raw output from docker compose ps command showing service count and states | [optional] [default to undefined]
**state** | **string** | Derived project state parsed from the raw docker compose status | [optional] [default to undefined]
**path** | **string** | Full filesystem path to the docker-compose.yml file | [optional] [default to undefined]

## Example

```typescript
import { VPSV1DockerManagerProjectResource } from 'hostinger-api-sdk';

const instance: VPSV1DockerManagerProjectResource = {
    name,
    status,
    state,
    path,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
