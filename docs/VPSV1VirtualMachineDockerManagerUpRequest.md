# VPSV1VirtualMachineDockerManagerUpRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_name** | **string** | Docker Compose project name using alphanumeric characters, dashes, and underscores only | [default to undefined]
**content** | **string** | URL pointing to docker-compose.yaml file, Github repository or raw YAML content of the compose file | [default to undefined]

## Example

```typescript
import { VPSV1VirtualMachineDockerManagerUpRequest } from 'hostinger-api-sdk';

const instance: VPSV1VirtualMachineDockerManagerUpRequest = {
    project_name,
    content,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
