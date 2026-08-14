# EcommerceV1ProductProductImageUploadUrlResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**upload_url** | **string** | Signed URL to upload the image to with a multipart/form-data POST. | [optional] [default to undefined]
**fields** | **{ [key: string]: string; }** | Form fields to send alongside the file in the multipart POST. | [optional] [default to undefined]
**object_name** | **string** | Key of the uploaded object — send it to the attach-image endpoint. | [optional] [default to undefined]
**max_bytes** | **number** | Maximum accepted upload size in bytes. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductProductImageUploadUrlResource } from 'hostinger-api-sdk';

const instance: EcommerceV1ProductProductImageUploadUrlResource = {
    upload_url,
    fields,
    object_name,
    max_bytes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
