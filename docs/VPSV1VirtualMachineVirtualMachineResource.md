# VPSV1VirtualMachineVirtualMachineResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Virtual machine ID | [optional] [default to undefined]
**firewall_group_id** | **number** | Active firewall ID, &#x60;null&#x60; if disabled | [optional] [default to undefined]
**subscription_id** | **string** | Subscription ID | [optional] [default to undefined]
**plan** | **string** | VPS plan name | [optional] [default to undefined]
**hostname** | **string** |  | [optional] [default to undefined]
**state** | **string** |  | [optional] [default to undefined]
**actions_lock** | **string** |  | [optional] [default to undefined]
**cpus** | **number** | CPUs count assigned to virtual machine | [optional] [default to undefined]
**memory** | **number** | Memory available to virtual machine (in megabytes) | [optional] [default to undefined]
**disk** | **number** | Virtual machine disk size (in megabytes) | [optional] [default to undefined]
**bandwidth** | **number** | Monthly internet traffic available to virtual machine (in megabytes) | [optional] [default to undefined]
**ns1** | **string** | Primary DNS resolver | [optional] [default to undefined]
**ns2** | **string** | Secondary DNS resolver | [optional] [default to undefined]
**ipv4** | [**Array&lt;VPSV1IPAddressIPAddressResource&gt;**](VPSV1IPAddressIPAddressResource.md) | Array of [&#x60;VPS.V1.IPAddress.IPAddressResource&#x60;](#model/vpsv1ipaddressipaddressresource) | [optional] [default to undefined]
**ipv6** | [**Array&lt;VPSV1IPAddressIPAddressResource&gt;**](VPSV1IPAddressIPAddressResource.md) | Array of [&#x60;VPS.V1.IPAddress.IPAddressResource&#x60;](#model/vpsv1ipaddressipaddressresource) | [optional] [default to undefined]
**template** | [**VPSV1TemplateTemplateResource**](VPSV1TemplateTemplateResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { VPSV1VirtualMachineVirtualMachineResource } from 'hostinger-api-sdk';

const instance: VPSV1VirtualMachineVirtualMachineResource = {
    id,
    firewall_group_id,
    subscription_id,
    plan,
    hostname,
    state,
    actions_lock,
    cpus,
    memory,
    disk,
    bandwidth,
    ns1,
    ns2,
    ipv4,
    ipv6,
    template,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
