# VPSV1FirewallFirewallResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Firewall ID | [optional] [default to undefined]
**name** | **string** | Firewall name | [optional] [default to undefined]
**is_synced** | **boolean** | Is current firewall synced with VPS | [optional] [default to undefined]
**rules** | [**Array&lt;VPSV1FirewallFirewallRuleResource&gt;**](VPSV1FirewallFirewallRuleResource.md) | Array of [&#x60;VPS.V1.Firewall.FirewallRuleResource&#x60;](#model/vpsv1firewallfirewallruleresource) | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**updated_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { VPSV1FirewallFirewallResource } from 'hostinger-api-sdk';

const instance: VPSV1FirewallFirewallResource = {
    id,
    name,
    is_synced,
    rules,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
