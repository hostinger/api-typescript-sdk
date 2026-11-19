# DNSV1PropagationPropagationReportResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**authoritative** | [**DNSV1PropagationAuthoritativeAnswerResource**](DNSV1PropagationAuthoritativeAnswerResource.md) |  | [optional] [default to undefined]
**vantage_points** | [**Array&lt;DNSV1PropagationVantagePointResource&gt;**](DNSV1PropagationVantagePointResource.md) | Answers of public resolvers at locations around the world | [optional] [default to undefined]

## Example

```typescript
import { DNSV1PropagationPropagationReportResource } from '@hostinger/sdk';

const instance: DNSV1PropagationPropagationReportResource = {
    authoritative,
    vantage_points,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
