# VPSV1VirtualMachineSetupRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **number** | Template ID | [default to undefined]
**data_center_id** | **number** | Data center ID | [default to undefined]
**post_install_script_id** | **number** | Post-install script ID | [optional] [default to undefined]
**password** | **string** | Password for the virtual machine. If not provided, random password will be generated. Password will not be shown in the response. | [optional] [default to undefined]
**hostname** | **string** | Override default hostname of the virtual machine | [optional] [default to undefined]
**install_monarx** | **boolean** | Install Monarx malware scanner (if supported) | [optional] [default to false]
**enable_backups** | **boolean** | Enable weekly backup schedule | [optional] [default to true]
**ns1** | **string** | Name server 1 | [optional] [default to undefined]
**ns2** | **string** | Name server 2 | [optional] [default to undefined]
**public_key** | [**VPSV1VirtualMachineSetupRequestPublicKey**](VPSV1VirtualMachineSetupRequestPublicKey.md) |  | [optional] [default to undefined]

## Example

```typescript
import { VPSV1VirtualMachineSetupRequest } from 'hostinger-api-sdk';

const instance: VPSV1VirtualMachineSetupRequest = {
    template_id,
    data_center_id,
    post_install_script_id,
    password,
    hostname,
    install_monarx,
    enable_backups,
    ns1,
    ns2,
    public_key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
