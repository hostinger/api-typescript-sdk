# ReachV1ProfilesDomainsSuspendedSenderEmailResource

A sender address on the connected domain that is no longer allowed to send.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** |  | [optional] [default to undefined]
**email_local_part** | **string** | The part of the address before the @. | [optional] [default to undefined]
**suspended_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesDomainsSuspendedSenderEmailResource } from '@hostinger/sdk';

const instance: ReachV1ProfilesDomainsSuspendedSenderEmailResource = {
    email,
    email_local_part,
    suspended_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
