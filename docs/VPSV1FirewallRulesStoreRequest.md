# VPSV1FirewallRulesStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**protocol** | **string** |  | [default to undefined]
**port** | **string** | Port or port range, ex: 1024:2048 | [default to undefined]
**source** | **string** |  | [default to undefined]
**source_detail** | **string** | IP range, CIDR, single IP or &#x60;any&#x60; | [default to undefined]

## Example

```typescript
import { VPSV1FirewallRulesStoreRequest } from 'hostinger-api-sdk';

const instance: VPSV1FirewallRulesStoreRequest = {
    protocol,
    port,
    source,
    source_detail,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
