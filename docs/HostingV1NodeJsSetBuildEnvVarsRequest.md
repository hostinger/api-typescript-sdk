# HostingV1NodeJsSetBuildEnvVarsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**env_vars** | [**Array&lt;HostingV1NodeJsSetBuildEnvVarsRequestEnvVarsInner&gt;**](HostingV1NodeJsSetBuildEnvVarsRequestEnvVarsInner.md) | Environment variables to set. This is the full desired set: any variable not in this list is deleted, and an empty array deletes every variable. | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsSetBuildEnvVarsRequest } from 'hostinger-api-sdk';

const instance: HostingV1NodeJsSetBuildEnvVarsRequest = {
    env_vars,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
