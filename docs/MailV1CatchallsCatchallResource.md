# MailV1CatchallsCatchallResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique catch-all identifier | [optional] [default to undefined]
**mailbox** | [**MailV1CatchallsCatchallMailboxResource**](MailV1CatchallsCatchallMailboxResource.md) |  | [optional] [default to undefined]
**domain** | **string** | Domain whose unrouted messages are caught | [optional] [default to undefined]
**is_active** | **boolean** | Whether the catch-all is active | [optional] [default to undefined]
**is_confirmed** | **boolean** | Whether the mailbox address has confirmed the catch-all | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1CatchallsCatchallResource } from 'hostinger-api-sdk';

const instance: MailV1CatchallsCatchallResource = {
    id,
    mailbox,
    domain,
    is_active,
    is_confirmed,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
