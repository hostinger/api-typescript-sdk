# MailV1ApiTokensApiTokenScopeResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**has_all_mailboxes** | **boolean** | Whether the token covers all current and future mailboxes of the order | [optional] [default to undefined]
**mailboxes** | [**Array&lt;MailV1ApiTokensApiTokenMailboxResource&gt;**](MailV1ApiTokensApiTokenMailboxResource.md) | Mailboxes this token grants access to. Empty when &#x60;has_all_mailboxes&#x60; is true. | [optional] [default to undefined]

## Example

```typescript
import { MailV1ApiTokensApiTokenScopeResource } from 'hostinger-api-sdk';

const instance: MailV1ApiTokensApiTokenScopeResource = {
    has_all_mailboxes,
    mailboxes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
