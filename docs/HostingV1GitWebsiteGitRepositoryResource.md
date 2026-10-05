# HostingV1GitWebsiteGitRepositoryResource

Git repository linked to a directory of the website. A repository whose clone failed stays listed; deploying it again retries the clone.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**repository_url** | **string** | Clone URL of the repository. A username, password or token in an HTTP(S) URL, or a password in any URL, is shown as &#x60;***&#x60;. | [default to undefined]
**branch** | **string** | Branch that is cloned and pulled | [default to undefined]
**directory** | **string** | Directory under the website document root. Empty means the document root. | [default to undefined]
**webhook** | [**HostingV1GitWebsiteGitRepositoryWebhookResource**](HostingV1GitWebsiteGitRepositoryWebhookResource.md) |  | [default to undefined]

## Example

```typescript
import { HostingV1GitWebsiteGitRepositoryResource } from '@hostinger/sdk';

const instance: HostingV1GitWebsiteGitRepositoryResource = {
    repository_url,
    branch,
    directory,
    webhook,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
