# DNSV1ZoneResetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sync** | **boolean** | Determines if operation should be run synchronously | [optional] [default to true]
**reset_email_records** | **boolean** | Determines if email records should be reset | [optional] [default to true]
**whitelisted_record_types** | **Array&lt;string&gt;** | Specifies which record types to not reset | [optional] [default to undefined]

## Example

```typescript
import { DNSV1ZoneResetRequest } from 'hostinger-api-sdk';

const instance: DNSV1ZoneResetRequest = {
    sync,
    reset_email_records,
    whitelisted_record_types,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
