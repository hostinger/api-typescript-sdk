# MailV1SchemaUpdateWebhookRequestSchema

Fields to update. All fields are optional; only provided fields are changed. Pass `\"description\": null` to clear the description.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | New human-readable name for the webhook | [optional] [default to undefined]
**description** | **string** | New description, or null to clear it | [optional] [default to undefined]
**events** | **Array&lt;string&gt;** | Replaces the full list of subscribed events | [optional] [default to undefined]
**status** | **string** | New status for the webhook | [optional] [default to undefined]
**url** | **string** | New URL to deliver events to | [optional] [default to undefined]

## Example

```typescript
import { MailV1SchemaUpdateWebhookRequestSchema } from 'hostinger-api-sdk';

const instance: MailV1SchemaUpdateWebhookRequestSchema = {
    name,
    description,
    events,
    status,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
