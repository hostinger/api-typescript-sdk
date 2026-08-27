# ReachV1ProfilesDomainsSendingDomainResource

The sending domain connected to the profile.  When no domain is connected every field is `null` and `suspended_sender_emails` is empty, so the shape stays the same whether or not the profile is set up for sending.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain campaigns are sent from. It may be a subdomain of the domain that was connected, so it will not always match the website domain. | [optional] [default to undefined]
**status** | **string** | Campaigns can only be sent while the domain is &#x60;active&#x60;. | [optional] [default to undefined]
**created_at** | **string** | When the domain was connected to the profile. | [optional] [default to undefined]
**updated_at** | **string** | When the domain or its verification state last changed. | [optional] [default to undefined]
**suspended_sender_emails** | [**Array&lt;ReachV1ProfilesDomainsSuspendedSenderEmailResource&gt;**](ReachV1ProfilesDomainsSuspendedSenderEmailResource.md) | Sender addresses on this domain that have been suspended. A campaign using one of them will not go out even while the domain itself is active. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesDomainsSendingDomainResource } from '@hostinger/sdk';

const instance: ReachV1ProfilesDomainsSendingDomainResource = {
    domain,
    status,
    created_at,
    updated_at,
    suspended_sender_emails,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
