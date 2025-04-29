# VPSV1VirtualMachineRecreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**template_id** | **number** | Template ID | [default to undefined]
**password** | **string** | Password for the virtual machine. If not provided, random password will be generated. Password will not be shown in the response. | [optional] [default to undefined]
**post_install_script_id** | **number** | Post-install script ID | [optional] [default to undefined]

## Example

```typescript
import { VPSV1VirtualMachineRecreateRequest } from 'hostinger-api-sdk';

const instance: VPSV1VirtualMachineRecreateRequest = {
    template_id,
    password,
    post_install_script_id,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
