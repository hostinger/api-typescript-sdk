# HostingV1NodeJsPatchResultResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pr_url** | **string** | URL to the created GitHub pull request | [optional] [default to undefined]
**pr_number** | **number** | GitHub pull request number | [optional] [default to undefined]
**head_branch** | **string** | The branch created with the fix | [optional] [default to undefined]
**patched_vulnerability_ids** | **Array&lt;string&gt;** | List of vulnerability IDs that were patched in the pull request | [optional] [default to undefined]

## Example

```typescript
import { HostingV1NodeJsPatchResultResource } from 'hostinger-api-sdk';

const instance: HostingV1NodeJsPatchResultResource = {
    pr_url,
    pr_number,
    head_branch,
    patched_vulnerability_ids,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
