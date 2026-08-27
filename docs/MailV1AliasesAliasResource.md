# MailV1AliasesAliasResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique alias identifier | [optional] [default to undefined]
**address** | **string** | Email address of the alias | [optional] [default to undefined]
**mailbox** | [**MailV1AliasesAliasMailboxResource**](MailV1AliasesAliasMailboxResource.md) |  | [optional] [default to undefined]
**is_active** | **boolean** | Whether the alias is active and not suspended | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1AliasesAliasResource } from '@hostinger/sdk';

const instance: MailV1AliasesAliasResource = {
    id,
    address,
    mailbox,
    is_active,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
