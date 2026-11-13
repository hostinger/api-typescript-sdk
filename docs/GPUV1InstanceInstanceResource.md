# GPUV1InstanceInstanceResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | GPU instance ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**status** | **string** |  | [optional] [default to undefined]
**action_lock** | **string** | Whether an action is in progress on the instance | [optional] [default to undefined]
**action_lock_reason** | **string** | Action in progress on the instance, &#x60;null&#x60; when unlocked | [optional] [default to undefined]
**pool** | [**GPUV1PoolPoolResource**](GPUV1PoolPoolResource.md) |  | [optional] [default to undefined]
**pool_instance** | [**GPUV1PoolPoolInstanceResource**](GPUV1PoolPoolInstanceResource.md) |  | [optional] [default to undefined]
**os_template** | [**GPUV1OsTemplateOsTemplateResource**](GPUV1OsTemplateOsTemplateResource.md) |  | [optional] [default to undefined]
**llm_model_variant** | [**GPUV1LlmModelVariantLlmModelVariantResource**](GPUV1LlmModelVariantLlmModelVariantResource.md) |  | [optional] [default to undefined]
**ssh_keys** | [**Array&lt;GPUV1SshKeySshKeyResource&gt;**](GPUV1SshKeySshKeyResource.md) | Array of [&#x60;GPU.V1.SshKey.SshKeyResource&#x60;](#model/gpuv1sshkeysshkeyresource) | [optional] [default to undefined]

## Example

```typescript
import { GPUV1InstanceInstanceResource } from '@hostinger/sdk';

const instance: GPUV1InstanceInstanceResource = {
    id,
    name,
    status,
    action_lock,
    action_lock_reason,
    pool,
    pool_instance,
    os_template,
    llm_model_variant,
    ssh_keys,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
