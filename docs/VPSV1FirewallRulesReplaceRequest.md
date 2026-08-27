# VPSV1FirewallRulesReplaceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rules** | [**Array&lt;VPSV1FirewallRulesStoreRequest&gt;**](VPSV1FirewallRulesStoreRequest.md) | The complete set of firewall rules that atomically replaces all existing rules in the group | [default to undefined]
**sync** | **boolean** | Synchronize the firewall group to all its virtual machines after replacing the rules | [optional] [default to undefined]

## Example

```typescript
import { VPSV1FirewallRulesReplaceRequest } from '@hostinger/sdk';

const instance: VPSV1FirewallRulesReplaceRequest = {
    rules,
    sync,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
