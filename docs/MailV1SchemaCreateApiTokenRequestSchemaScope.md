# MailV1SchemaCreateApiTokenRequestSchemaScope

Mailbox scope this token can access

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_all_mailboxes** | **boolean** | Grant access to all current and future mailboxes of the order | [default to undefined]
**mailbox_ids** | **Array&lt;string&gt;** | Required when &#x60;has_all_mailboxes&#x60; is false. Mailbox resource IDs of this order. | [optional] [default to undefined]

## Example

```typescript
import { MailV1SchemaCreateApiTokenRequestSchemaScope } from 'hostinger-api-sdk';

const instance: MailV1SchemaCreateApiTokenRequestSchemaScope = {
    has_all_mailboxes,
    mailbox_ids,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
