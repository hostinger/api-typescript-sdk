# HostingV1GitUpdateGitAutoDeploymentSettingsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**installation_uuid** | **string** | Active Git installation from &#x60;List Git installations&#x60; | [default to undefined]
**owner** | **string** | Repository owner login, as returned by &#x60;List Git installation repositories&#x60;. GitLab group paths use slashes. | [default to undefined]
**repository** | **string** | Repository name without the .git suffix | [default to undefined]
**branch** | **string** | Branch to deploy | [default to undefined]
**directory** | **string** | Subdirectory under the website document root to deploy into. Empty, null or omitted means the document root. | [optional] [default to '']
**is_enabled** | **boolean** | Whether pushes to the branch deploy automatically | [optional] [default to true]

## Example

```typescript
import { HostingV1GitUpdateGitAutoDeploymentSettingsRequest } from '@hostinger/sdk';

const instance: HostingV1GitUpdateGitAutoDeploymentSettingsRequest = {
    installation_uuid,
    owner,
    repository,
    branch,
    directory,
    is_enabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
