# HostingV1FilesFilesResourceItemsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Entry name. | [default to undefined]
**path** | **string** | Entry path, relative to the document root. | [default to undefined]
**type** | **string** | Entry type. | [default to undefined]
**size_bytes** | **number** | Entry size in bytes. Null for directories, symlinks, and other non-file entries. | [default to undefined]

## Example

```typescript
import { HostingV1FilesFilesResourceItemsInner } from 'hostinger-api-sdk';

const instance: HostingV1FilesFilesResourceItemsInner = {
    name,
    path,
    type,
    size_bytes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
