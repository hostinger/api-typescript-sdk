# MailV1WebhooksWebhookDeliveryLogResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created_at** | **string** |  | [optional] [default to undefined]
**mailbox_address** | **string** | Email address of the mailbox this delivery is attached to | [optional] [default to undefined]
**webhook_url** | **string** | URL that received the webhook POST request | [optional] [default to undefined]
**is_successful** | **boolean** | Whether the delivery was successful | [optional] [default to undefined]
**duration** | **number** | Webhook request duration in milliseconds | [optional] [default to undefined]
**retry_count** | **number** | Number of delivery attempts made | [optional] [default to undefined]
**max_retry_count** | **number** | Maximum number of delivery attempts allowed | [optional] [default to undefined]

## Example

```typescript
import { MailV1WebhooksWebhookDeliveryLogResource } from 'hostinger-api-sdk';

const instance: MailV1WebhooksWebhookDeliveryLogResource = {
    created_at,
    mailbox_address,
    webhook_url,
    is_successful,
    duration,
    retry_count,
    max_retry_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
