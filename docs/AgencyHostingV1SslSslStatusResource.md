# AgencyHostingV1SslSslStatusResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | &#x60;installing&#x60; while a certificate setup is running or retrying, &#x60;active&#x60; when a valid certificate is in place (uploaded, platform-issued, or a lifetime certificate bought for the domain), &#x60;failed&#x60; when the last setup gave up and no valid certificate is in place, &#x60;expired&#x60; when the certificate has run out, &#x60;not_installed&#x60; when the domain has no certificate and no setup process. | [default to undefined]
**is_custom** | **boolean** | Whether the certificate was uploaded by the customer instead of issued or sold by the platform. | [default to undefined]
**expires_at** | **string** | End of the validity period of the certificate in place; null when there is none or the uploaded certificate carries no expiry. | [default to undefined]

## Example

```typescript
import { AgencyHostingV1SslSslStatusResource } from '@hostinger/sdk';

const instance: AgencyHostingV1SslSslStatusResource = {
    status,
    is_custom,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
