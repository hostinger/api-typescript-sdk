# MailV1MailboxesMailboxUsageResource

Periodically synced usage numbers (may lag behind live values)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**storage_used** | **number** | Storage used in kilobytes | [optional] [default to undefined]
**storage_quota** | **number** | Storage quota in kilobytes | [optional] [default to undefined]
**messages_used** | **number** |  | [optional] [default to undefined]
**messages_quota** | **number** |  | [optional] [default to undefined]
**synced_at** | **string** | When the usage numbers were last synced; null if never synced | [optional] [default to undefined]

## Example

```typescript
import { MailV1MailboxesMailboxUsageResource } from 'hostinger-api-sdk';

const instance: MailV1MailboxesMailboxUsageResource = {
    storage_used,
    storage_quota,
    messages_used,
    messages_quota,
    synced_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
