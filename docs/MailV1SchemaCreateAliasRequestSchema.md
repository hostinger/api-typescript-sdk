# MailV1SchemaCreateAliasRequestSchema


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**local_part** | **string** | Local part of the alias address (the part before the @). The domain is taken from the mailbox. Case-insensitive and stored lowercase; must start and end with a letter or digit; single dots, underscores and hyphens are allowed in between. | [default to undefined]

## Example

```typescript
import { MailV1SchemaCreateAliasRequestSchema } from '@hostinger/sdk';

const instance: MailV1SchemaCreateAliasRequestSchema = {
    local_part,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
