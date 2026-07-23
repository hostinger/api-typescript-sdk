# MailV1OrdersPlanDomainResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**mailbox_quota** | **number** | Maximum number of mailboxes per domain | [optional] [default to undefined]
**forwarder_quota** | **number** | Maximum number of forwarders per domain | [optional] [default to undefined]
**alias_quota** | **number** | Maximum number of aliases per domain | [optional] [default to undefined]
**is_catchall_enabled** | **boolean** | Whether catch-all mailboxes are available | [optional] [default to undefined]
**is_imap_enabled** | **boolean** | Whether IMAP access is available | [optional] [default to undefined]
**is_pop3_enabled** | **boolean** | Whether POP3 access is available | [optional] [default to undefined]

## Example

```typescript
import { MailV1OrdersPlanDomainResource } from 'hostinger-api-sdk';

const instance: MailV1OrdersPlanDomainResource = {
    mailbox_quota,
    forwarder_quota,
    alias_quota,
    is_catchall_enabled,
    is_imap_enabled,
    is_pop3_enabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
