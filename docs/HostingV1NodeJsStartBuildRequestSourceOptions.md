# HostingV1NodeJsStartBuildRequestSourceOptions

Source-specific options. For `archive` send `archive_path`. For `git` send `owner`, `repository`, `branch` and `installation_uuid`, taken from `List Git installations` and `List Git installation repositories`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**archive_path** | **string** | The path to the archive file relative to the document root of the vhost (required if source is \&quot;archive\&quot;) | [optional] [default to undefined]
**owner** | **string** | Repository owner login (required if source is \&quot;git\&quot;). GitLab group paths use slashes. | [optional] [default to undefined]
**repository** | **string** | Repository name without the .git suffix (required if source is \&quot;git\&quot;) | [optional] [default to undefined]
**branch** | **string** | Branch to build (required if source is \&quot;git\&quot;) | [optional] [default to undefined]
**installation_uuid** | **string** | Git installation used to access the repository (required if source is \&quot;git\&quot;) | [optional] [default to undefined]

## Example

```typescript
import { HostingV1NodeJsStartBuildRequestSourceOptions } from '@hostinger/sdk';

const instance: HostingV1NodeJsStartBuildRequestSourceOptions = {
    archive_path,
    owner,
    repository,
    branch,
    installation_uuid,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
