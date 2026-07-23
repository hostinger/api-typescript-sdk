# MailV1OrdersPlanResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Machine name of the plan | [optional] [default to undefined]
**title** | **string** | Human-readable plan title | [optional] [default to undefined]
**domain** | [**MailV1OrdersPlanDomainResource**](MailV1OrdersPlanDomainResource.md) |  | [optional] [default to undefined]
**mailbox** | [**MailV1OrdersPlanMailboxResource**](MailV1OrdersPlanMailboxResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1OrdersPlanResource } from 'hostinger-api-sdk';

const instance: MailV1OrdersPlanResource = {
    name,
    title,
    domain,
    mailbox,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
