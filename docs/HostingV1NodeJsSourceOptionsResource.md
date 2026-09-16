# HostingV1NodeJsSourceOptionsResource

Which keys carry values depends on the parent source_type; the others are null.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**archive_path** | **string** | Present if sourceType is \&quot;archive\&quot; | [optional] [default to undefined]
**owner** | **string** | Repository owner login (present if source_type is \&quot;git\&quot;) | [default to undefined]
**repository** | **string** | Repository name without the .git suffix (present if source_type is \&quot;git\&quot;) | [default to undefined]
**branch** | **string** | Branch that was built (present if source_type is \&quot;git\&quot;) | [default to undefined]
**installation_uuid** | **string** | Git installation used to access the repository (present if source_type is \&quot;git\&quot;) | [default to undefined]
**commit** | [**HostingV1GitGitCommitResource**](HostingV1GitGitCommitResource.md) |  | [default to undefined]

## Example

```typescript
import { HostingV1NodeJsSourceOptionsResource } from '@hostinger/sdk';

const instance: HostingV1NodeJsSourceOptionsResource = {
    archive_path,
    owner,
    repository,
    branch,
    installation_uuid,
    commit,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
