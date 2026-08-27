# HostingV1FilesFileContentResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **string** | File path, relative to the document root. | [default to undefined]
**content** | **string** | File content for the requested line range. | [default to undefined]
**from_line** | **number** | Line offset the returned content starts from. | [default to undefined]
**total_lines** | **number** | Total number of lines in the file. | [default to undefined]
**size_bytes** | **number** | Total file size in bytes. | [default to undefined]

## Example

```typescript
import { HostingV1FilesFileContentResource } from '@hostinger/sdk';

const instance: HostingV1FilesFileContentResource = {
    path,
    content,
    from_line,
    total_lines,
    size_bytes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
