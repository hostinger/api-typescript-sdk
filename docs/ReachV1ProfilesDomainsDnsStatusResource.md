# ReachV1ProfilesDomainsDnsStatusResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** |  | [optional] [default to undefined]
**mx** | [**ReachV1ProfilesDomainsDnsRecordStatus**](ReachV1ProfilesDomainsDnsRecordStatus.md) |  | [optional] [default to undefined]
**spf** | [**ReachV1ProfilesDomainsDnsRecordStatus**](ReachV1ProfilesDomainsDnsRecordStatus.md) |  | [optional] [default to undefined]
**dkim** | [**ReachV1ProfilesDomainsDnsRecordStatus**](ReachV1ProfilesDomainsDnsRecordStatus.md) |  | [optional] [default to undefined]
**dmarc** | [**ReachV1ProfilesDomainsDnsRecordStatus**](ReachV1ProfilesDomainsDnsRecordStatus.md) |  | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesDomainsDnsStatusResource } from 'hostinger-api-sdk';

const instance: ReachV1ProfilesDomainsDnsStatusResource = {
    domain,
    mx,
    spf,
    dkim,
    dmarc,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
