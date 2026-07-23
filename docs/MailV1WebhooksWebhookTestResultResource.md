# MailV1WebhooksWebhookTestResultResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**http_status** | **number** | HTTP status code returned by the webhook endpoint | [optional] [default to undefined]
**is_successful** | **boolean** | Whether the test delivery was successful | [optional] [default to undefined]
**error** | **string** | Error message returned by the webhook endpoint in case of failure | [optional] [default to undefined]

## Example

```typescript
import { MailV1WebhooksWebhookTestResultResource } from 'hostinger-api-sdk';

const instance: MailV1WebhooksWebhookTestResultResource = {
    http_status,
    is_successful,
    error,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
