# MailV1WebhooksWebhookCreatedResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique webhook identifier | [optional] [default to undefined]
**mailbox** | [**MailV1WebhooksWebhookMailboxResource**](MailV1WebhooksWebhookMailboxResource.md) |  | [optional] [default to undefined]
**name** | **string** | Human-readable name for this webhook | [optional] [default to undefined]
**description** | **string** | Optional description of the webhook\&#39;s purpose | [optional] [default to undefined]
**events** | **Array&lt;string&gt;** | Events that trigger this webhook | [optional] [default to undefined]
**status** | **string** | Current status of the webhook | [optional] [default to undefined]
**url** | **string** | URL that receives webhook POST requests | [optional] [default to undefined]
**secret** | **string** | One-time webhook secret, returned only on creation. Sent as &#x60;Authorization: Bearer &lt;secret&gt;&#x60; with every delivery. | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1WebhooksWebhookCreatedResource } from 'hostinger-api-sdk';

const instance: MailV1WebhooksWebhookCreatedResource = {
    id,
    mailbox,
    name,
    description,
    events,
    status,
    url,
    secret,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
