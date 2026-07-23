# MailV1ApiTokensApiTokenCreatedResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique API token identifier | [optional] [default to undefined]
**token** | **string** | Plaintext API token, returned only in this response. Grants access to the [Hostinger Email API](https://api.mail.hostinger.com/) for mailbox provisioning and management. | [optional] [default to undefined]
**name** | **string** | Human-readable label for this token | [optional] [default to undefined]
**scope** | [**MailV1ApiTokensApiTokenScopeResource**](MailV1ApiTokensApiTokenScopeResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1ApiTokensApiTokenCreatedResource } from 'hostinger-api-sdk';

const instance: MailV1ApiTokensApiTokenCreatedResource = {
    id,
    token,
    name,
    scope,
    created_at,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
