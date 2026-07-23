# MailV1OrdersPlanMailboxResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**storage_quota** | **number** | Storage quota per mailbox in megabytes | [optional] [default to undefined]
**messages_quota** | **number** | Maximum number of stored messages per mailbox | [optional] [default to undefined]
**forwarder_quota** | **number** | Maximum number of forwarders per mailbox | [optional] [default to undefined]
**alias_quota** | **number** | Maximum number of aliases per mailbox | [optional] [default to undefined]
**max_outbound_message_size** | **number** | Maximum outbound message size in bytes | [optional] [default to undefined]
**max_outbound_attachment_size** | **number** | Maximum outbound attachment size in bytes | [optional] [default to undefined]
**max_outbound_recipient_limit** | **number** | Maximum number of recipients per outbound message | [optional] [default to undefined]
**rate_limit_inbound** | **string** | Inbound message rate limit as &#x60;messages/seconds&#x60; | [optional] [default to undefined]
**rate_limit_outbound** | **string** | Outbound message rate limit as &#x60;messages/seconds&#x60; | [optional] [default to undefined]

## Example

```typescript
import { MailV1OrdersPlanMailboxResource } from 'hostinger-api-sdk';

const instance: MailV1OrdersPlanMailboxResource = {
    storage_quota,
    messages_quota,
    forwarder_quota,
    alias_quota,
    max_outbound_message_size,
    max_outbound_attachment_size,
    max_outbound_recipient_limit,
    rate_limit_inbound,
    rate_limit_outbound,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
