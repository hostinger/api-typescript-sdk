# WordPressV1ContentGenerateImagesRequest

Generate images from a prompt and an image type

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt** | **string** | What the image should show. For the logo type, the wordmark and mark to render. | [default to undefined]
**image_type** | **string** | Kind of image to generate. It sets the default size and cropping. | [default to undefined]
**num_of_images** | **number** | How many images to generate | [optional] [default to 1]
**width** | **number** | Output width in pixels. Defaults per image type and is ignored for the logo type. | [optional] [default to undefined]
**height** | **number** | Output height in pixels. Defaults per image type and is ignored for the logo type. | [optional] [default to undefined]
**style** | **string** | Style tokens appended to photographic prompts. Ignored for the logo type. | [optional] [default to undefined]
**color_guidance** | **string** | Colour direction for the logo type only. It is not rendered as text. | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1ContentGenerateImagesRequest } from '@hostinger/sdk';

const instance: WordPressV1ContentGenerateImagesRequest = {
    prompt,
    image_type,
    num_of_images,
    width,
    height,
    style,
    color_guidance,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
