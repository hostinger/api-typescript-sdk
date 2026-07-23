# MailV1SchemaCreateWebhookRequestSchema


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Human-readable name for this webhook | [default to undefined]
**description** | **string** | Optional description of the webhook\&#39;s purpose | [optional] [default to undefined]
**events** | **Array&lt;string&gt;** | Events that trigger this webhook | [default to undefined]
**status** | **string** | Initial status of the webhook | [optional] [default to StatusEnum_Active]
**url** | **string** | Publicly reachable URL that receives the webhook POST requests | [default to undefined]

## Example

```typescript
import { MailV1SchemaCreateWebhookRequestSchema } from 'hostinger-api-sdk';

const instance: MailV1SchemaCreateWebhookRequestSchema = {
    name,
    description,
    events,
    status,
    url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
