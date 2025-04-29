# VPSV1FirewallFirewallRuleResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Firewall rule ID | [optional] [default to undefined]
**action** | **string** | Firewall rule action | [optional] [default to undefined]
**protocol** | **string** | Firewall rule protocol | [optional] [default to undefined]
**port** | **string** | Firewall rule destination port: single or port range | [optional] [default to undefined]
**source** | **string** | Firewall rule source. Can be &#x60;any&#x60; or &#x60;custom&#x60; | [optional] [default to undefined]
**source_detail** | **string** | Firewall rule source detail. Can be &#x60;any&#x60; or IP address, CIDR or range | [optional] [default to undefined]

## Example

```typescript
import { VPSV1FirewallFirewallRuleResource } from 'hostinger-api-sdk';

const instance: VPSV1FirewallFirewallRuleResource = {
    id,
    action,
    protocol,
    port,
    source,
    source_detail,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
