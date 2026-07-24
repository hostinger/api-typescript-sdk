# MailV1SchemaCreateForwarderRequestSchema


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**destination** | **string** | Email address the messages will be forwarded to | [default to undefined]
**is_keep_copy_enabled** | **boolean** | Whether to keep a copy of forwarded messages in the mailbox. Defaults to false. | [optional] [default to undefined]

## Example

```typescript
import { MailV1SchemaCreateForwarderRequestSchema } from 'hostinger-api-sdk';

const instance: MailV1SchemaCreateForwarderRequestSchema = {
    destination,
    is_keep_copy_enabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
