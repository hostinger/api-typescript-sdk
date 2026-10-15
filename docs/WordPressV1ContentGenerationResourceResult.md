# WordPressV1ContentGenerationResourceResult

Generated content, `null` until the status is `completed`. For `image-generation` it is the generated images object; for `website-generation` it is the generated website document.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | [**Array&lt;WordPressV1ContentGeneratedImageResource&gt;**](WordPressV1ContentGeneratedImageResource.md) | Generated images, each available at a temporary URL | [default to undefined]
**expires_at** | **string** | Time after which the image URLs stop working. Download the images before then. | [default to undefined]

## Example

```typescript
import { WordPressV1ContentGenerationResourceResult } from '@hostinger/sdk';

const instance: WordPressV1ContentGenerationResourceResult = {
    images,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
