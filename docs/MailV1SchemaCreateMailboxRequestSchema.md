# MailV1SchemaCreateMailboxRequestSchema


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**local_part** | **string** | Local part of the mailbox address (the part before the @). The domain is taken from the order. Must start and end with a letter or digit; single dots, underscores and hyphens are allowed in between. | [default to undefined]
**password** | **string** | Mailbox password. Minimum 8 characters with uppercase, lowercase, number and special character. | [default to undefined]

## Example

```typescript
import { MailV1SchemaCreateMailboxRequestSchema } from 'hostinger-api-sdk';

const instance: MailV1SchemaCreateMailboxRequestSchema = {
    local_part,
    password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
