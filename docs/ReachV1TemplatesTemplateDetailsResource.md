# ReachV1TemplatesTemplateDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | Pass this as the &#x60;template_uuid&#x60; of a campaign. | [optional] [default to undefined]
**title** | **string** | Null for templates that were never named. | [optional] [default to undefined]
**template_content** | **string** | Full HTML of the template, with personalization tags such as &#x60;{{name}}&#x60; unrendered. Null when the stored HTML cannot be read. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1TemplatesTemplateDetailsResource } from '@hostinger/sdk';

const instance: ReachV1TemplatesTemplateDetailsResource = {
    uuid,
    title,
    template_content,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
