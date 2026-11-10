# DomainsV1DomainDomainVerificationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | What registration waits for: - &#x60;manual_review&#x60;: a check you cannot complete yourself, such as a review of the order by   Hostinger. You have nothing to do. - &#x60;sms_code&#x60;: a code was sent by SMS to the phone number of the owner WHOIS profile. Enter it   in [hPanel](https://hpanel.hostinger.com/). - &#x60;contact_verification&#x60;: the registry requires the owner WHOIS profile to be verified first,   by email, phone number or contact name. Complete it in   [hPanel](https://hpanel.hostinger.com/); registration resumes once the profile is verified. | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1DomainDomainVerificationResource } from '@hostinger/sdk';

const instance: DomainsV1DomainDomainVerificationResource = {
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
