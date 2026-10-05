# HostingV1GitDeployWebsiteGitRepositoryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**repository_url** | **string** | Clone URL of the repository on any Git host, SSH or HTTPS. Private repositories need an SSH URL and the account\&#39;s Git SSH key added to the repository as a deploy key. An HTTP or HTTPS URL with a username or token, or any URL with a password, is rejected. | [default to undefined]
**branch** | **string** | Branch to clone and pull | [default to undefined]
**directory** | **string** | Directory under the website document root, exactly as &#x60;List website Git repositories&#x60; returns it for an existing repository. Empty, null or omitted means the document root. | [optional] [default to '']

## Example

```typescript
import { HostingV1GitDeployWebsiteGitRepositoryRequest } from '@hostinger/sdk';

const instance: HostingV1GitDeployWebsiteGitRepositoryRequest = {
    repository_url,
    branch,
    directory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
