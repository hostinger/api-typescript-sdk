# WordPressV1ContentGenerationResource

State of an AI content generation and, once completed, its result.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**generation_id** | **string** | Generation ID (UUID) used to poll for the result | [default to undefined]
**type** | **string** | Kind of generation, determines the shape of &#x60;result&#x60; | [default to undefined]
**status** | **string** | &#x60;in-progress&#x60; while the generation is still running, &#x60;completed&#x60; once &#x60;result&#x60; is available, &#x60;failed&#x60; when the generation stopped without a result. | [default to undefined]
**result** | [**WordPressV1ContentGenerationResourceResult**](WordPressV1ContentGenerationResourceResult.md) |  | [default to undefined]

## Example

```typescript
import { WordPressV1ContentGenerationResource } from '@hostinger/sdk';

const instance: WordPressV1ContentGenerationResource = {
    generation_id,
    type,
    status,
    result,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
