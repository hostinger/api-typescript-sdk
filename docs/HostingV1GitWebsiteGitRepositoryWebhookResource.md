# HostingV1GitWebsiteGitRepositoryWebhookResource

Auto-deployment webhook of the repository, the same one the Git section of hPanel shows

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | Webhook URL to add on the Git host for automatic deployment | [default to undefined]
**provider** | **string** | Git host detected from the repository URL. Null when it is not GitHub, GitLab or Bitbucket. | [default to undefined]
**setup_url** | **string** | Page on the Git host where the webhook is added. Null when the host is not detected. | [default to undefined]
**tutorial_url** | **string** | Git host guide for adding a webhook. Null when the host is not detected. | [default to undefined]

## Example

```typescript
import { HostingV1GitWebsiteGitRepositoryWebhookResource } from '@hostinger/sdk';

const instance: HostingV1GitWebsiteGitRepositoryWebhookResource = {
    url,
    provider,
    setup_url,
    tutorial_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
