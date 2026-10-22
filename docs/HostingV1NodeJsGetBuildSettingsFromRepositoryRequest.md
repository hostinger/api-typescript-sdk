# HostingV1NodeJsGetBuildSettingsFromRepositoryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | **string** | Repository owner login, as returned by &#x60;List Git installation repositories&#x60;. GitLab group paths use slashes. | [default to undefined]
**repository** | **string** | Repository name without the .git suffix | [default to undefined]
**branch** | **string** | Branch whose package.json is inspected | [default to undefined]
**installation_uuid** | **string** | Git installation used to access the repository, taken from &#x60;List Git installations&#x60; | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsGetBuildSettingsFromRepositoryRequest } from '@hostinger/sdk';

const instance: HostingV1NodeJsGetBuildSettingsFromRepositoryRequest = {
    owner,
    repository,
    branch,
    installation_uuid,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
