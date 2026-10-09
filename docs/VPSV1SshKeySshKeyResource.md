# VPSV1SshKeySshKeyResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **string** | SSH public key in OpenSSH format | [optional] [default to undefined]
**type** | **string** | SSH key type | [optional] [default to undefined]
**data** | **string** | SSH key data (base64 encoded public key) | [optional] [default to undefined]
**name** | **string** | SSH key comment/name | [optional] [default to undefined]

## Example

```typescript
import { VPSV1SshKeySshKeyResource } from '@hostinger/sdk';

const instance: VPSV1SshKeySshKeyResource = {
    key,
    type,
    data,
    name,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
