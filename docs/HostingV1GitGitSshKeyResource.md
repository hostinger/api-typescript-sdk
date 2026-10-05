# HostingV1GitGitSshKeyResource

Public SSH key the hosting account uses to clone and pull Git repositories

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_key** | **string** | Public key to add as a deploy key on the Git host. Null when the account has no key yet. | [default to undefined]

## Example

```typescript
import { HostingV1GitGitSshKeyResource } from '@hostinger/sdk';

const instance: HostingV1GitGitSshKeyResource = {
    public_key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
