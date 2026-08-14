# EcommerceV1ProductUploadProductImageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_url** | **string** | Publicly reachable URL of the raster image (JPEG, PNG, GIF or WebP), maximum 15MB. The image is fetched, virus-scanned and validated by content, then stored on the CDN. SVG is not accepted. | [default to undefined]
**is_thumbnail** | **boolean** | When true, the image becomes the product\&#39;s thumbnail (primary image). When omitted, it becomes the thumbnail only if the product does not have one yet. | [optional] [default to undefined]

## Example

```typescript
import { EcommerceV1ProductUploadProductImageRequest } from 'hostinger-api-sdk';

const instance: EcommerceV1ProductUploadProductImageRequest = {
    image_url,
    is_thumbnail,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
