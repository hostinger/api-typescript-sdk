# HostingV1GitGitRepositoryResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Repository identifier assigned by the Git provider | [default to undefined]
**name** | **string** | Repository name without the .git suffix | [default to undefined]
**full_name** | **string** | Owner and repository name joined with a slash | [default to undefined]
**owner** | **string** | Repository owner login | [default to undefined]
**is_private** | **boolean** | Whether the repository is private | [default to undefined]
**html_url** | **string** | Repository page URL | [default to undefined]
**clone_url** | **string** | HTTPS clone URL | [default to undefined]
**default_branch** | **string** | Default branch of the repository | [default to undefined]

## Example

```typescript
import { HostingV1GitGitRepositoryResource } from '@hostinger/sdk';

const instance: HostingV1GitGitRepositoryResource = {
    id,
    name,
    full_name,
    owner,
    is_private,
    html_url,
    clone_url,
    default_branch,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
