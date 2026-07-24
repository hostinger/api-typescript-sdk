# MailV1ForwardersForwarderResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique forwarder identifier | [optional] [default to undefined]
**mailbox** | [**MailV1ForwardersForwarderMailboxResource**](MailV1ForwardersForwarderMailboxResource.md) |  | [optional] [default to undefined]
**destination** | **string** | Email address the messages are forwarded to | [optional] [default to undefined]
**is_keep_copy_enabled** | **boolean** | Whether a copy of forwarded messages is kept in the mailbox | [optional] [default to undefined]
**is_active** | **boolean** | Whether the forwarder is active | [optional] [default to undefined]
**is_confirmed** | **boolean** | Whether the destination address has confirmed the forwarding | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1ForwardersForwarderResource } from 'hostinger-api-sdk';

const instance: MailV1ForwardersForwarderResource = {
    id,
    mailbox,
    destination,
    is_keep_copy_enabled,
    is_active,
    is_confirmed,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
