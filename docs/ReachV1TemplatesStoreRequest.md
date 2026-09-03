# ReachV1TemplatesStoreRequest

Create a reusable email template

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_content** | **string** | The email body as HTML. It is sanitised before it is stored, so the saved template can differ from what was sent - inline any styles the email clients need and keep the markup self-contained. | [default to undefined]
**title** | **string** | Name the template is listed under. Not shown to the recipients. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1TemplatesStoreRequest } from '@hostinger/sdk';

const instance: ReachV1TemplatesStoreRequest = {
    template_content,
    title,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
