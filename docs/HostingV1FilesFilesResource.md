# HostingV1FilesFilesResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **string** | Listed directory, relative to the document root. | [default to undefined]
**items** | [**Array&lt;HostingV1FilesFilesResourceItemsInner&gt;**](HostingV1FilesFilesResourceItemsInner.md) | Entries found in the listed directory. | [default to undefined]
**total_items** | **number** | Total number of entries matching the listing, across all pages. | [default to undefined]
**total_items_current_page** | **number** | Number of entries in this page. | [default to undefined]
**offset** | **number** | Number of entries skipped before this page. | [default to undefined]

## Example

```typescript
import { HostingV1FilesFilesResource } from '@hostinger/sdk';

const instance: HostingV1FilesFilesResource = {
    path,
    items,
    total_items,
    total_items_current_page,
    offset,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
