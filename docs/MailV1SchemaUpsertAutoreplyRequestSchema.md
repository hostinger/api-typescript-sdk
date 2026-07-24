# MailV1SchemaUpsertAutoreplyRequestSchema


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subject** | **string** | Subject of the automatic reply | [default to undefined]
**body** | **string** | Body of the automatic reply | [default to undefined]
**display_name** | **string** | Sender display name used for the reply | [optional] [default to undefined]
**starts_at** | **string** | When the autoreply becomes active. Defaults to now. | [optional] [default to undefined]
**ends_at** | **string** | When the autoreply stops. Omit for an indefinite autoreply. | [optional] [default to undefined]

## Example

```typescript
import { MailV1SchemaUpsertAutoreplyRequestSchema } from 'hostinger-api-sdk';

const instance: MailV1SchemaUpsertAutoreplyRequestSchema = {
    subject,
    body,
    display_name,
    starts_at,
    ends_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
