# HostingV1GitGitDeployOutputResource

Result of cloning or pulling a Git repository into the website

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_success** | **boolean** | Whether the clone or pull, and composer install when it ran, finished without errors | [default to undefined]
**output** | **string** | Log of the deployment steps, and the Git or composer error when &#x60;is_success&#x60; is false | [default to undefined]

## Example

```typescript
import { HostingV1GitGitDeployOutputResource } from '@hostinger/sdk';

const instance: HostingV1GitGitDeployOutputResource = {
    is_success,
    output,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
