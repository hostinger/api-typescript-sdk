# MailV1MailboxesMailboxResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Mailbox resource ID | [optional] [default to undefined]
**address** | **string** | Email address of the mailbox | [optional] [default to undefined]
**status** | **string** | Mailbox status | [optional] [default to undefined]
**status_reason** | **string** | Reason the mailbox was suspended | [optional] [default to undefined]
**protocols** | [**MailV1MailboxesMailboxProtocolsResource**](MailV1MailboxesMailboxProtocolsResource.md) |  | [optional] [default to undefined]
**counts** | [**MailV1MailboxesMailboxCountsResource**](MailV1MailboxesMailboxCountsResource.md) |  | [optional] [default to undefined]
**is_catchall** | **boolean** | Whether the mailbox is the catch-all destination for its domain | [optional] [default to undefined]
**usage** | [**MailV1MailboxesMailboxUsageResource**](MailV1MailboxesMailboxUsageResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1MailboxesMailboxResource } from 'hostinger-api-sdk';

const instance: MailV1MailboxesMailboxResource = {
    id,
    address,
    status,
    status_reason,
    protocols,
    counts,
    is_catchall,
    usage,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
