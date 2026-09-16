# HostingV1GitGitAutoDeploymentSettingsResource

Every field is null when the website has no Git auto-deployment configured.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**installation_uuid** | **string** | Git installation the repository is accessed through | [default to undefined]
**is_enabled** | **boolean** | Whether pushes to the branch deploy automatically | [default to undefined]
**owner** | **string** | Repository owner login | [default to undefined]
**repository** | **string** | Repository name | [default to undefined]
**branch** | **string** | Branch that is deployed | [default to undefined]
**directory** | **string** | Subdirectory under the website document root the repository deploys into. Empty means the document root. | [default to undefined]

## Example

```typescript
import { HostingV1GitGitAutoDeploymentSettingsResource } from '@hostinger/sdk';

const instance: HostingV1GitGitAutoDeploymentSettingsResource = {
    installation_uuid,
    is_enabled,
    owner,
    repository,
    branch,
    directory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
