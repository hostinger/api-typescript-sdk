# MailV1AutorepliesAutoreplyResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique autoreply identifier | [optional] [default to undefined]
**mailbox** | [**MailV1AutorepliesAutoreplyMailboxResource**](MailV1AutorepliesAutoreplyMailboxResource.md) |  | [optional] [default to undefined]
**subject** | **string** | Subject of the automatic reply | [optional] [default to undefined]
**body** | **string** | Body of the automatic reply | [optional] [default to undefined]
**display_name** | **string** | Sender display name used for the reply | [optional] [default to undefined]
**starts_at** | **string** | When the autoreply becomes active | [optional] [default to undefined]
**ends_at** | **string** | When the autoreply stops | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1AutorepliesAutoreplyResource } from 'hostinger-api-sdk';

const instance: MailV1AutorepliesAutoreplyResource = {
    id,
    mailbox,
    subject,
    body,
    display_name,
    starts_at,
    ends_at,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
